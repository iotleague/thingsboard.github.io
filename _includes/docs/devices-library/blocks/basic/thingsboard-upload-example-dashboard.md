
{% assign importDashboardCE = '
    ===
        image: /images/user-guide/dashboards/creating-dash-ce.png,
        title: Open the "Dashboards" page. Click on the "+" icon in the top right corner. Select "Import dashboard".
    ===
        image: /images/user-guide/dashboards/dashboard-import-ce.png,
        title: The dashboard import window should pop up, and you will be prompted to upload the JSON file and click "Import".
    ===
        image: /images/user-guide/dashboards/dashboard-import-1-ce.png,
        title: Dashboard has been imported.
'
%}

{% assign importDashboardPE = '
    ===
        image: /images/user-guide/dashboards/creating-dash-pe.png,
        title: Open the "Dashboards" page. By default, you navigate to the dashboard group "All". Click on the "+" icon in the top right corner. Select "Import dashboard".
    ===
        image: /images/user-guide/dashboards/dashboard-import-pe.png,
        title: The dashboard import window should pop up, and you will be prompted to upload the JSON file and click "Import".
    ===
        image: /images/user-guide/dashboards/dashboard-import-1-pe.png,
        title: Dashboard has been imported.
'
%}

{% assign exampleDashboardPath = "/docs/devices-library/resources/dashboards/microcontrollers/basic/dashboard.json" %}
{% if boardLedCount == 3 %}
{% assign exampleDashboardPath = "/docs/devices-library/resources/dashboards/microcontrollers/rgb-led/dashboard.json" %}
{% endif %}

{% if hasDisplay == "true" %}
{% assign exampleDashboardPath = "/docs/devices-library/resources/dashboards/microcontrollers/display/dashboard.json" %}
{% endif %}

{% if hasCamera == "true" %}
{% assign exampleDashboardPath = "/docs/devices-library/resources/dashboards/microcontrollers/camera/dashboard.json" %}
{% endif %}

{% if include.exampleDashboardPath %}
{% assign exampleDashboardPath = include.exampleDashboardPath %}
{% endif %}

On dashboards, you can display data, send commands to devices, update device attributes, etc. So, we will create the dashboard, for our device.  

To add the dashboard to ThingsBoard, we need to import it, and to do this, we have to go through the following steps:

- First download the [Check and control device data dashboard]({{exampleDashboardPath}}){:target="_blank" download="dashboard.json"} file.

{% if page.docsPrefix == "pe/" or page.docsPrefix == "paas/" %}
    {% include images-gallery.liquid showListImageTitles="true" imageCollection=importDashboardPE %}
{% else %}  
    {% include images-gallery.liquid showListImageTitles="true" imageCollection=importDashboardCE %}
{% endif %}