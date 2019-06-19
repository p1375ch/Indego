# Indego
Fork from iMarkus/Indego (thanks for the inspiration and all your work with the basics!)

Home Assistant Custom Component for Bosch Indego Lawn Mower

Place the files in custom-component in your Home Assistant folder for custom-componentes

    config/custom_components
    
Add new platform to your configuration.yaml

    indego:
      username: !secret indego_username
      password: !secret indego_password
      id: !secret indego_id

Add your account (usually mail address), password and serial number to secrets.yaml: 

    indego_username: x.y@mail.com
    indego_password: mysecretpw
    indego_id: 123456789

Finally add your new sensor called indego_state: 

    sensor:
      - platform: indego
    
Debugging:

    logger:
      default: error
      logs:
        custom_components.indego: debug
