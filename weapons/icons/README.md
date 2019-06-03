# Custom Weapon Icons
> **IMPORTANT**: Make sure to put your icons in the folder `materials/vgui/ttt/` <br>
> E.g. [rollermine weapon icon](https://github.com/BadgerCode/TTT-Rollermine/tree/master/materials/vgui/ttt)


# Backgrounds
![Blue-Background](background-blue.png)
![Blue-Background](background-red.png)
![Blue-Background](background-green.png)
![Blue-Background](background-gold.png)


# Example icon
This folder contains the example icon `icon_example_deagle`

![Blue-Background](background-blue.png)
![Blue-Background](foreground-deagle.png)
![Blue-Background](icon_example_deagle.png)

<br>

These files are required by the client & server to use the icon
* icon_example_deagle.vmt
* icon_example_deagle.vtf


# Converting PNG/JPG to VTF
You will need the program [VTF Edit](https://developer.valvesoftware.com/wiki/VTFEdit).

1. Open **VTF Edit** and go to File->Import
2. Select your file with the follow settings
    * General
        * Alpha Format: BGRA8888 
            * _It's about halfway down the drop-down_
        * Generate Mipmaps: ❌
    * Advanced
        * Generate Thumbnail: ❌
    * Click import
3. Select the **Flags**
    * Point Sample ✅
    * No Mipmap ✅
    * No Level of Detail ✅
    * Eight Bit Alpha ✅
4. Save your image
    * This should be in your addon's folder
    * It should go in `materials/vgui/ttt/`
5. Tools => Generate VMT File
    * Make sure the path in `Base Texture 1` is correct
    * Options
        * Shader: UnlitGeneric
        * vertexcolor ✅
        * vertexalpha ✅
        * translucent ✅


## Expected Output
You should end up with the following files:
* materials/vgui/ttt/icon_your_file_name.vmt
* materials/vgui/ttt/icon_your_file_name.vtf

<br>

`icon_your_file_name.vmt` should look like the following
```
"UnlitGeneric"
{
 "$basetexture" "VGUI/ttt/icon_your_file_name"
 "$vertexcolor" 1
 "$vertexalpha" 1
 "$translucent" 1
}
```