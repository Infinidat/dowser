Overview
========

This is a pip/easy_install'able version of http://e-mats.org/2013/01/debugging-pythons-memory-usage-with-dowser/

Usage
-----

To quickly start-up a CherryPy-based server:

    from dowser import launch_memory_usage_server
    launch_memory_usage_server()


If you want to integrate dowser in your existing CherryPy app:

    from dowser import Root
    class ExistingCherryPyApp(object):
        dowser = Root()
        dowser.exposed = True
        trace = dowser.trace
        chart = dowser.chart
        
This will bind `/dowser`, `/trace` and `/chart` to the dowser CherryPy app
