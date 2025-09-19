# What is serializer?

####  Serializer convert complex data structure ,like objeact or databse records , into formet that is easier to store ,transmit or process such as json and xml.


#### Simple meaning 
A serializer in DRF is a translator(Like use Json ,xml etc) between Django models and API.

It's covert python object into json object.

#### Complex meaning

## Serializer 

Complex Data type to (serializer) python native data type to  json data type(render into json)

## Dserializer

Json data type to python native data type into Complex Data Type (Desrializer)

Update,create,Delete are use dserializer formet when Read (retrive) are use serializer 


# Serializer validate

### Types

## 1.Field level
## 2.object level
## 3.validate

1.Field level
    field meaning is this is validate only specific field like name,roll,phone number,adhar id etc...(Validates one field at a time.)

    >>>>>>>> validate_<field_name>
    class CompanydataSerializer(serializers.ModelSerializer):
    
    class Meta:
        model = Companydata
        fields = "__all__"

    def validate_team_manager(self, value):

        data = [m.strip() for m in value.split(",") if m.strip()]
        print(data)
        if len(data) <= 2:
            print('yes')
            return value
        else:
            print('else yes')
            raise serializers.ValidationError("Select any 2 or less then 2 manager")



2. object level
    they validates multiples field together


    
        def validate(self, data):
            " Object level validation"
            title = data.get('title')
            author = data.get('author')

            if title.lower() == 'admin' or author.lower() == 'admin':
                raise serializers.ValidationError('You does not Use Admin username ..')
            return data

3. built in model validation
    
    django provide many validate like balnk,uniqe,max_lenght,min_lenght,email,etc...


4. Custom validator Functions

write independent function and the pass them to serializer fiald

        def must_start_with_d(value):
            if not value.lower().startswith('d'):
                raise serializers.ValidationError("Must start with letter D.")

        class BookSerializer(serializers.Serializer):
            title = serializers.CharField(validators=[must_start_with_d])


