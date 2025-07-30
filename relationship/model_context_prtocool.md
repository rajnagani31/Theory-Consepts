# model context processors

write in spreat file
    
    def total_today_task(request):
        task=15
        return({'tasks':task})

    Note: define in settings.py
    TEMPLATES = [
    {
        ...........
            "context_processors": [
                .....
                "app1.file_name.function_name
            ],
        },
    },
]    

# Why is use
    context processos allow any value in your frountend 
    like:cart,userprofile items,home page (they show all page and it's mean user show this data in anywere)

1.direactly show task in base tamplate or sun tremplates like tsak:{{task}}

but you use base templates show task but all other data show with today task in all templates,you use base teamplates and show all today task total ,always difine in your view (return render(req,'h1.html',{'task':task})) so now is here context no need context in evry view function and logic

but i only want today task total and page data no need base data in all templeat


so you can also use context processors
