# Setting-Lighting

Status: URP

![Screenshot 2024-01-05 at 18.48.08.png](Setting-Lighting%20871febe8cde2476ea4239e649d38c258/Screenshot_2024-01-05_at_18.48.08.png)

# Lighting

Lighting is the setting to configure all settings related to light, however, some light settings are in **Project Setting→Graphics, URP/HDRP setting** in the Assets folder. Even **Preferences→GI Cache is also related** to light. Another setting named Lighting **Lighting Explore** is also used for all lighting settings in the scene. It would not be obvious when beginners try to learn Unity lighting. To understand **Lighting** Settings ****in Unity, you can think they are static settings for the project, once you set them, you will not likely touch them anymore.

## Scene

Used to set the lighting type of **GI**, there are **Baked GI** and **Realtime GI**. Depending on your project, you can choose Baked GI for better performance, while Realtime GI for better Graphic quality but lower performance.

### Light Settings

Save all configurations into prefab, so you can save your settings and reuse them later.

### **Realtime Lighting (Realtime Global Illumination Lighting)**

This setting is specific for the **light type of** **Directional Light** to generate the **Indirect light(GI)**, once it is opened, Directional Light can generate indirect light in realtime. It is not free and your scene must be satisfied:

- Only **static objects** can contribute to GI
- **Directional Light** setting→**Indirect Multiplier** must be bigger than 1(light will bounce at least once)

 Here is example if GI was not successed because objects are not static or Indirect Multiplier is 0

![Screenshot 2024-01-05 at 20.44.12.png](Setting-Lighting%20871febe8cde2476ea4239e649d38c258/Screenshot_2024-01-05_at_20.44.12.png)

Here is example if GI was successed because objects are static and indirect multiplier is 70.

![Screenshot 2024-01-05 at 20.46.53.png](Setting-Lighting%20871febe8cde2476ea4239e649d38c258/Screenshot_2024-01-05_at_20.46.53.png)

Realtime Global Illumination