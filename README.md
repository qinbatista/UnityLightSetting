# Lighting


Lighting is the setting to configure all settings related to light, however, some light settings are in **Project Setting→Graphics, URP/HDRP setting** in the Assets folder. Even **Preferences→GI Cache is also related** to light. Another setting named **Lighting Explore** is also used for all lighting settings in the scene. It would not be obvious when beginners try to learn Unity lighting. To understand **Lighting** Settings in Unity, you can think they are static settings for the project, once you set them, you will not likely touch them anymore.


## SCENE
<picture><img src="https://github.com/qinbatista/UnityLightSetting/blob/master/Images/lightsetting.png" width = 1000px align="center"></picture>
Used to set the lighting type of **GI**, there are **Baked GI** and **Realtime GI**. Depending on your project, you can choose Baked GI for better performance, while Realtime GI for better Graphic quality but lower performance.

### Light Settings

Save all your light configurations into prefab, so you can save your settings and reuse them later.

### Realtime Lighting (Realtime Global Illumination Lighting)
<picture><img src="https://github.com/qinbatista/UnityLightSetting/blob/master/Images/GISetting.png" width = 900px align="center"></picture>

This setting is specific for the **light type of** **Directional Light** to generate the **Indirect light(GI)**, once it is opened, Directional Light can generate indirect light in realtime. It is not free and your scene must be satisfied:

- Only **static objects** can contribute to GI from Directional Light
- **Directional Light** setting→**Indirect Multiplier** must be bigger than 1(light will bounce at least once)

*Here is an example of GI did not succeed because objects are not static or the Indirect Multiplier is 0*

<picture><img src="https://github.com/qinbatista/UnityLightSetting/blob/master/Images/GIFailed.png" width = 900px align="center"></picture>

*Here is an example of GI that was successful because objects are static and the indirect multiplier is 70.5*

<picture><img src="https://github.com/qinbatista/UnityLightSetting/blob/master/Images/GISuccess.png" width = 900px align="center"></picture>

| Option | Description |
| ------ | ----------- |
| Realtime Global Illumination   | Open Realtime GI for Directional Light |
| Realtime environment Light | If **Mixed Lighting->Baked Global Illumination** is opened, open realtime GI or not |
| Indirect Resolution    | Quality of GI or light baking map, higher value leads to high quality but longer baking time. Bake once every time the indirect resolution changes, after baking a real-time light map, the scene can use real-time GI for all static objects, and all the values will be saved to real-time Lightmaps |

<picture><img src="https://github.com/qinbatista/UnityLightSetting/blob/master/Images/lightingmap.png" width = 900px align="center"></picture>

*Here are examples of different Indirect Resolutions, open in **Scene->Draw Model->Realtime Global Illumination**.*

<picture><img src="https://github.com/qinbatista/UnityLightSetting/blob/master/Images/GIResolution2.png" width = 900px align="center"></picture>
<picture><img src="https://github.com/qinbatista/UnityLightSetting/blob/master/Images/GIResolution8.png" width = 900px align="center"></picture>

#### Real GI showcase

- Scene Location`Assets->Scene->1RealtimeGI`

![Minion](https://github.com/qinbatista/UnityLightSetting/blob/master/Images/ShowGI.gif)