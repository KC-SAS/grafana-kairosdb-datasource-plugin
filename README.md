grafana-kairosdb-datasource-plugin
==================================
[![Gitter](https://badges.gitter.im/Join Chat.svg)](https://gitter.im/Kratos-ISE/grafana-kairosdb-datasource-plugin?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

This is a plugin that allows Grafana to support KairosDB as datasource.

To install, copy the files into the plugins directory of Grafana in a subfolder called kairosdb.

You can either use the provided configuration file or add the following to the existing configuration file:

        plugins: {
            // list of plugin panels
            panels: [],
            // requirejs modules in plugins folder that should be loaded
            // for example custom datasources
            dependencies: ['kairosdb/kairosdbDatasource'],
        }


and then specifiy the datasource:

        datasources: {
            kairosdb: {
                type: 'KairosDBDatasource',
                url: "http://"+window.location.hostname+":8080",
                default: true
            },
        },

Download commit tagged v1.8.1 to be compatible with Grafana-1.8.1.
Download latest source to be compatible with Grafana 1.9.0 

IMPORTANT: this plugin is only compatible with Grafana versions < V2.0. To support the newest verions, please refer to https://github.com/br0th3r/grafana2-kairosdb-datasource-plugin

Note: KairosDB 0.9.3 does not support align_start_time so please uncheck this option
