# rankwatch17_py_monitoring

    import threading
    import psutil

    def printinfo():
        threading.Timer(5.0,printitm).start() #to repeat for every 5 sec
        
        print 'No of cpu cores are: ',psutil.cpu_count()
        print 'RAM usage:  ',psutil.virtual_memory()
        print 'Disk Usage: ',psutil.disk_usage('C:\\')
        print 'CPU Usage: ',psutil.cpu_percent(interval=None,percpu=True)
        
    printinfo()
    #to print avg CPU usage in last 30sec
    print psutil.cpu_percent(interval=5.0,percpu=False)
    #to print avg CPU usage in last 1 min
    print psutil.cpu_percent(interval=60,percpu=False)
    #to print avg CPU usage in last 5 min
    print psutil.cpu_percent(interval=300,percpu=False)
