.. _working_in_xsheet:

Working in Xsheet
=================
The xsheet, the digital version of the traditional exposure sheet, allows you to control the timing of all of the elements of a scene. It is organized in columns and rows: each column contains a layer of the animation and each row represents a frame contents. Columns are divided into cells, representing the content of that column in a particular frame. 

Different items, generically called here as levels, can be loaded into the scene: animation levels, images for the background and overlays, and clips.

Other OpenToonz scenes can be loaded as well: they will be nested inside a column and considered a sub-xsheet of the current scene.

All of the xsheet contents can be checked in the viewer, where the animation can be played back, and the scene contents edited.


.. _using_the_viewer:

Using the Viewer
----------------
The viewer, or work area, has different modes of visualizing the scene contents. According to your needs you can view the whole work area, only the elements included in the current camera shot, or visualize the whole scene in a 3D environment. The viewer can also be frozen, so that the visualization is not updated until you enter with the pointer in the work area. When the preview mode is activated, it can display the rendered animation as in the final render (see  :ref:`Previewing the Animation <previewing_the_animation>`  ).




At the bottom of the work area another customizable set of buttons is available. Some are used for the playback (see  :ref:`Using the Work Area <using_the_work_area>`  ), some others are relevant only using the Animate tool (|animate|) to animate objects and when previewing the animation in the viewer (see :ref:`Animating Objects <animating_objects>`  and :ref:`Previewing the Animation <previewing_the_animation>`  ).



Additional elements like a field guide, or the table, can be displayed or hidden, and the background color can be set (see  :ref:`Customizing the Work Area <customizing_the_work_area>`  ).

.. tip:: **To switch the view mode in the work area:**

    Use the buttons available in the work area title bar to do the following:

    - The Camera Stand View button (|camera_stand|) is for standard view, where any part of the work area can be displayed. When playing back the scene, the work area stands still, while all of the other elements, including the camera, move in relation to its position.



    - The 3D View button (|3d|) is for activating or deactivating the 3D view of the elements composing the scene (see  :ref:`Working in a 3D Environment <working_in_a_3d_environment>`  ).

    - The Camera View button (|camera_view|) is for keeping the box representing the camera still, while all of the other elements move in relation to its position. It can help you to better understand the shot when there are camera trucks, or rotations.

.. note:: When a frame of the level strip is selected, the view mode is set in order to display the level only, and consequently the buttons on the viewer title bar are disabled. To enable them again, select a cell in the xsheet. 

.. tip:: **To freeze/un-freeze the viewer:**

    Click the Freeze button (|freeze|) in the work area title bar to freeze/unfreeze the displayed content; when activated the word frozen is displayed at the center of the work area.



.. tip:: **To update the viewer content when it is frozen:**

    Move the pointer to the viewer area.


.. _using_the_file_browser:

Using the File Browser
----------------------
All the elements you need for a scene can be retrieved by using a file browser. 

You can either use the standard OpenToonz file browser to drag and drop levels or folders to the xsheet or the scene cast window, or use the Load Level and Load Folder browser you can open from the File menu. In both cases you can perform a multiple selection to load several levels or folders at the same time that will be exposed each in a separate column; if you use the Load Level browser, when loading an animation level you can also specify the frame range to load. When you use the Load Folder command all the files contained in the folder (if supported) are loaded into the xsheet.

.. note:: When a level is loaded, OpenToonz checks if its syntax matches one of the level formats specified into Preferences > Loading > Level Settings by Format. In this case the Level Settings specified will be applied. It is possible to add as many format as you want defining them by a Regular Expression. This way, different settings can be automatically applied to different kind of levels.

.. note:: It is possible to Ignore the Alpha Channel of levels loaded on the column 1 by activating the option in Preferences > Xsheet.

In the file tree available on the left there are the following main items:

- My Computer contains files and folders located in your computer.

- Network allows the access to network computers.

- My Documents contains files and folders located in the OS My Documents folder.

- History contains recently saved scenes, organized in folders, one for each of the last seven days OpenToonz was used.

- Library displays files and folder located in the ``Projectroot\library``  folder (see  :ref:`Setting the Projectroot <setting_the_projectroot>`  ).

- Projectroot lists all the projects that have been created as folders containing the project information and material; the actual value of the projectroot is displayed in brackets (see  :ref:`Using the Project Browser <using_the_project_browser>`  ).

.. note:: In case more than one projectroot is defined, each will be displayed with the related projectroot value in brackets (see  :ref:`Setting the Projectroot <setting_the_projectroot>`  ).

- Version control repository folder, labeled according to the version control configuration, contains the folders and files under version control (see  :ref:`Using the Version Control <using_the_version_control>`  ).

.. note:: In case several repositories are defined, each will be displayed with the related label (see  :ref:`Configuring the Version Control in OpenToonz <configuring_the_version_control_in_toonz>`  ).




You can open folders and sub-folders in order to retrieve files that are displayed in the area on the right. The current location path is displayed at the top of the browser; existing folders can be renamed and new folders can be created. Files can be displayed with related icons, or in a list displaying additional s that can be also used to sort files.

.. note:: The way file icons are generated in the OpenToonz browser depends on the images resolution and on the size set for the level strip frames in the Preferences > Interface dialog (see  :ref:`Using the Level Strip <using_the_level_strip>`  ).

As part of the scene you can load Toonz raster and vector animation levels (TLV and PLI), Toonz palettes (TPL), full-color images or sequences of full-color images (BMP, JPG, NOL, PNG, RGB, SGI, TGA, TIF and TIFF), clips (AVI, MOV, and MP4 and WebM with the aid of FFMPEG, if installed), Photoshop documents (PSD), vector images (SVG) and audio files (AIFF, WAV and MP3 with the aid of FFMPEG, if installed). Images or clips with alpha channel information once imported will retain their transparency information.

.. note:: It is also possible to load TZU and TZP files created with Toonz version 4.x: in this case the files will be automatically converted and loaded in the TLV format.

.. note:: Photoshop files can be loaded taking into account the layers the document is made of (see  :ref:`Loading Photoshop Documents <loading_photoshop_documents>`  ).

.. note:: SVG files are automatically converted and loaded in the PLI format.

Sequences of full color images can be recognized by OpenToonz file browsers as a single animation level if they are named with a progressive four-digits number written between the file name and the file extension, e.g. ``animation.0001.tif`` , ``animation.0002.tif`` , etc. They are displayed in the file browser with a double dot before the file extension, e.g. ``animation..tif`` .

From the browser you can view levels, images and clips you are going to load by opening a flipbook whose default shrink factor and step can be set in the preferences dialog, and see the related ed information by opening an info box (see  :ref:`Using the Flipbook <using_the_flipbook>`  ).

OpenToonz scenes (TNZ files) can be loaded as part of another scene as well: in this instance they are loaded as sub-xsheet (see  :ref:`Loading a Scene as a Sub-xsheet <loading_a_scene_as_a_sub-xsheet>`  ).

When you s from the standard OpenToonz file browser, you can set whether automatically to expose them in the xsheet or not, by setting the Expose Loaded Levels in Xsheet option in the Preferences > Loading dialog. If activated, each level will be placed in a different column, starting from the first empty one. If deactivated, the loaded levels will be stored in the scene cast, from where they can be selectively exposed in xsheet columns (see  :ref:`Using the Scene Cast <using_the_scene_cast>`  ).

If you are loading one or several files located outside the default folders of the current project, you are prompted whether to import them to the project database or to load them from where they are. In the former case files will be copied to the related default folder (PLI, TLV levels and palettes in the +drawings folder; full-color images, clips and audio files in the +extras folder; palettes in the +palettes folder) and loaded with a relative path from this new location (see  :ref:`Managing Projects <managing_projects>`  ); in the latter they will be loaded by creating an absolute loading path to their original location.

If any of the files you want to import has the same name of a file already existing in the destination default folder, you will prompted whether to keep the existing file, overwrite it with the new one, or rename it adding a suffix you can decide. In this way you can control if files you are importing were already imported previously, or manage files that share the same name. 

.. note:: Files loaded in a scene without importing can be imported later all at once by using the Collect Assets feature (see  :ref:`Collecting Assets <collecting_assets>`  ).

.. note:: The OpenToonz file browser displays only the relevant files that can be loaded in OpenToonz. To check the full content of the current folder you can use the Show Folder Content command (see below).

.. tip:: **To choose the browser display mode:**

    Do one of the following:

    - Click the thumbnails button (|thumbnails|) in the bottom bar of the browser to display files with the related icons.

    - Click the list button (|list|) in the bottom bar of the browser to display files in a list with related s; click the labels at the top of the  columns to sort files accordingly; right-click the label at the top of the  columns to open the menu that allows to toggle the visualization of the  columns.

.. tip:: **To resize the browser sections:**

    Do any of the following:

    - Click and drag the separator to resize sections. 

    - Click and drag the separator towards the window border to hide a section.

    - Click and drag the separator collapsed to the window border toward the window center to display again the hidden section.

.. tip:: **To rename an existing folder:**

    Double-click the folder name and rename it.

.. tip:: **To create a new folder:**

    Click the new folder button (|new_folder|) in the bottom bar of the browser.



.. tip:: **To move one folder up in the file tree:**

    Click the folder up button (|folder_up|) in the bottom bar of the browser.



.. tip:: **To load levels from the Load Level browser:**

    1. Select the xsheet cell where you want to start exposing the level; if any level is already exposed in that cell, a new column will be inserted to expose the new level.

    2. Do one of the following:

    - Choose File > Load Level.

    - Right-click in the xsheet cell and choose Load Level from the menu that opens.

    3. In the browser that opens select the level you want to load; if you select an animation level, select the frame range you want to load.

    4. Click the Load button.

.. tip:: **To load levels from the OpenToonz standard browser:**

    1. Select the xsheet cell where you want to start exposing the level; if any level is already exposed in that cell, a new column will be inserted to expose the new level.

    2. In the OpenToonz browser select the level you want to load.

    3. Do one of the following:

    - Drag and drop the selection to the scene cast pane or to the work area. 

    - Drag and drop the selection to the xsheet cell where you want to start exposing it. 

    - Right-click the selection and choose Load from the menu that opens.

.. note:: Files can also be loaded by dragging and dropping them from the Windows Explorer or Mac OS Finder to the scene cast, xsheet, or work area.

.. tip:: **To load folders:**

    1. Select the xsheet cell where you want to start exposing the levels; if any level is already exposed in that cell, a new column will be inserted to expose the new levels.

    2. In the OpenToonz File menu select the Load folder command.

    3. In the File Browser that opens select the folder you want to load.

    4. Press the OK button.

.. note:: Folders can also be loaded by dragging and dropping them from the Windows Explorer or Mac OS Finder to the scene cast, xsheet, or work area.

.. note:: When a level is loaded, OpenToonz checks if its syntax matches one of the level formats specified into Preferences>Loading>Level Settings by Format.In this case the Level Settings specified when the corresponding Edit pop up is opened will be applied. It is possible to add as many format as you want defining them by a Regular Expression. This way, different settings can be automatically applied to different kind of levels.

.. tip:: **To load back a recently loaded level:**

    Choose File > Open Recent Level File, then select the level you want to load from the available submenu.

.. tip:: **To make a multiple selection in the file browser:**

    Do one of the following:

    - Click to select a file.

    - Ctrl-click (PC) or Cmd-click (Mac) to add to or remove a file from the selection.

    - Shift-click to extend the selection.

    - Right-click in the right area of the browser and choose Select All from the menu that opens to select all the files contained in the current folder.

.. tip:: **To view a level in the flipbook:**

    Do one of the following:

    - In the OpenToonz browser or in the xsheet right-click the level you want to view and choose View from the menu that opens.

    - Choose Windows > Flipbook and drag and drop in the window the file you want to view.

.. note:: By opening several Flipbook windows you can view several levels at the same time.

.. tip:: **To set the default shrink factor and step for the file viewer:**

    1. Choose File > Preferences > Interface.

    2. Set the default Viewer Shrink and Step values.

.. tip:: **To view a level file information:**

    In the OpenToonz browser or in the xsheet right-click the level whose info you want to view and choose Info from the menu that opens; if the file is an animation level or a sequence of images, use the slider at the bottom of the box to change frame and see the related information.

.. tip:: **To view the entire contents of the current folder:**

    Right-click in the right area of the browser and choose Show Folder Contents from the menu that opens: the entire folder contents are displayed in a default OS window.


.. _loading_photoshop_documents:

Loading Photoshop Documents
'''''''''''''''''''''''''''
Photoshop documents (PSD files) can be loaded as a scene element in OpenToonz taking into account the layers the document is made of, and their layering order; text layers are considered as standard layers, while layer styles are considered only when loading the document as a single image (see below).

Supported formats are RGB or grayscale images, with 8 bits or 16 bits per channel. 

When a Photoshop document is loaded, a dialog opens to set the way the document has to be exposed in the xsheet. Options are the following:

- Single Image, flattens all the document layers into a single image. Only layers that were visible when the Photoshop document was saved are considered. The level name and path in Level Settings, and the scene cast, refer to the original name of the Photoshop document (see  :ref:`Editing Level Settings <editing_level_settings>`  and  :ref:`Using the Scene Cast <using_the_scene_cast>`  ).

.. note:: Photoshop documents can be loaded as a single image only if the Maximize Compatibility option was checked when saving the original file from Photoshop. If the option was deactivated, a dummy image is displayed instead; loading and saving again the document with the option activated fixes the problem.

- Frames, loads each document layer as a frame, and exposes them as a sequence in an xsheet column. Any layer group defined in the original document is ignored. The level name and path in Level Settings, and the scene cast, refer to the original name of the Photoshop document with the #frames suffix (see  :ref:`Editing Level Settings <editing_level_settings>`  and  :ref:`Using the Scene Cast <using_the_scene_cast>`  ).

 |Toonz71_233| 

    - Columns, loads each document layer as a column, and it is possible to automatically create a sub-xsheet containing the columns by activating the Expose in a Sub-xsheet option.

When a Photoshop document is loaded as columns, it is also possible to set the way groups of layers have to be considered. Options are the following:

    - Ignore groups, overlooks any group of layers defined in the document, and each layer is exposed in a different column. The level name and path in Level Settings, and the scene cast, for each level refer to the original name of the Photoshop document with the #layerName suffix (see  :ref:`Editing Level Settings <editing_level_settings>`  and  :ref:`Using the Scene Cast <using_the_scene_cast>`  ).

    - Expose layers in a group as columns in a sub-xsheet, creates for each group a sub-xsheet containing each layer of the group as a column. If a group contains other groups, the sub-xsheet will contain other sub-xsheets that will contain the related layers as columns. The level name and path in Level Settings, and the scene cast, for each level refer to the original name of the Photoshop document with the #layerID suffix (see  :ref:`Editing Level Settings <editing_level_settings>`  and  :ref:`Using the Scene Cast <using_the_scene_cast>`  ).

    - Expose layers in a group as frames in a column, creates for each group a column containing each layer of the group as a cell. If a group contains other groups, they will be ignored. The level name and path in Level Settings, and the scene cast, for each level refer to the original name of the Photoshop document with the #groupID#group suffix (see  :ref:`Editing Level Settings <editing_level_settings>`  and  :ref:`Using the Scene Cast <using_the_scene_cast>`  ).

.. note:: In order to be properly displayed in the final rendering, images based on Photoshop document layers have to be premultiplied either using the Premultiply option in the level settings, or the Premultiply effect (see  :ref:`Editing Level Settings <editing_level_settings>`  and  :ref:`Premultiply <premultiply>`  ).


.. _executing_tasks_in_the_file_browser:

Executing Tasks in the File Browser
'''''''''''''''''''''''''''''''''''
Some tasks concerning files can be executed directly in the file browser.

Files can be duplicated, converted to a different format, converted to TLV (Toonz raster image) format, renamed, and premultiplied. 

When duplicating files, the new files will be renamed by appending an underscore followed by progressive numbering.

When converting files, a dialog prompts the frame range to convert, a saving location, a name, the new format with related options and a color for the background of the converted file. It is also possible to select more files at once but, in this case, the frame range and the file name fields won’t be available. All levels, images and clips supported by OpenToonz can be converted. The PLI files can be converted to the SVG format.

When converting files to TLV format, it is possible to choose the painted or unpainted TLV formats; all levels, images and clips supported by OpenToonz can be converted, except PSD files.

The conversion to the unpainted TLV format is available when one or several files are selected and it is meant for lineart images: the images and levels are converted into black lineart images with a transparent background, so that they can be painted with the same techniques and tools you can use for Toonz raster levels (see  :ref:`Painting Animation Levels <painting_animation_levels>`  ). In particular if images have some transparency, transparent pixels remain transparent, while solid pixels are transformed into black ones; if images have no transparency, white and lighter pixels will be assumed as transparent, while dark pixels are transformed into black ones. 

The conversion to the painted TLV format is available when two files are selected or when the selected files are Raster Full color without antialiasing. In the case of the two files, one is meant to be the lineart and the other a painted version of the same image: the images and levels are converted into painted lineart images with a palette, so that they can be edited with the same techniques and tools you can use for Toonz raster levels (see  :ref:`Managing Palettes and Styles <managing_palettes_and_styles>`  and  :ref:`Painting Animation Levels <painting_animation_levels>`  ). In the case of conversion from Raster Full color without antialiasing an Heuristic is used to recognize lines and painted areas creating a TLV level where the lines are seen as ink and the painted areas as paint.

In particular if images have some transparency, transparent pixels remains transparent, while solid pixels are transformed into lines according to their color; if images have no transparency, white and lighter pixels will be assumed as transparent, while dark pixels are transformed into black lines. 

.. note:: When converting to the TLV format, sequence numbering modes different from the OpenToonz standard one (i.e. a progressive four-digits number written between the file name and the file extension) are supported, so that only the first file of a sequence is required to be selected to include the whole sequence in the conversion.

.. note:: The Convert command is also available in the File menu.

When renaming, files will be renamed according to the name you specify; an option allows you also to delete the original files. This can be used both for renaming sequences of image files in one shot, and for converting sequence numbering modes to the OpenToonz standard one (i.e. a progressive four-digits number written between the file name and the file extension) by selecting only the first file of a sequence.

When premultiplied, the file alpha channel is modified to be properly displayed in OpenToonz. Images which have a meaningful alpha channel come in two types: premultiplied or not. A non-premultiplied image can be recognized when it is loaded in OpenToonz because its edge, where there is a complete transparence on one side and opacity on the other, is not smooth, but displays a solid halo; by premultiplying the image it is possible to fix this problem. This is available only for full-color images.

.. tip:: **To duplicate files:**

    1. Select the files you want to duplicate. 

    2. Right-click any of the selected files and choose Duplicate from the menu that opens.

.. tip:: **To convert a file to a different format:**

    1. Right-click the file you want to convert and choose Convert from the menu that opens. The Convertwindow change depending on the format of the selected files.

    2. Choose the frame range to convert, the saving location, a name, the new format, and the background color of the converted file.

    3. Activate the Skip Existing Files to to prevent overwriting already exixting files.

    4. If needed, set the options for the file format chosen pressing the Options button and inserting the new values.

    5. Click the Convert button.

.. tip:: **To convert several files at once to a different format:**

    1. Select the files you want to convert.

    2. Right-click any of the selected files and choose Convert from the menu that opens.

    3. Check the number of files you are going to convert reading the value from the header of the Convert window.

    4. Choose the saving location, the new format, and the background color of the converted files.

    5. Activate the Skip Existing Files to to prevent overwriting already exixting files.

    6. If needed, set the options for the file format chosen pressing the Options button and inserting the new values.

    7. Click the Convert button.

.. tip:: **To convert files to the unpainted TLV format:**

    1. Select the lineart files you want to convert. 

    2. Right-click any of the selected files and choose Convert from the menu that opens.

    3. Select unpainted tlv from the File format drop down menu.




    4. Choose the saving location and, if you have selected one sequence, the frame range.

    5. Activate the Skip Existing Files to to prevent overwriting already existing files.

    6. Activate the Apply Autoclose.

    7. Choose how to manage Antialiasing fom the drop down menu. You can preserve the original antialiasing selecting Keep Original; add some antialiasing selecting Add and writing an Intensity value in the following text input field; remove the antialiasing selecting the Remove option and writing a Threshold value in the following text input field.

    8. Choose how to manage the palette of the tlv file/s you are going to create. By default a new palette is created. If you prefer to use an existing palette press the button next the palette field and use the browser to locate the palette file you desire to use.

    9. Click the Convert button.

.. tip:: **To convert files to the painted TLV format from two images:**

    1. Select the lineart file and the painted version of the same file you want to convert. 

    2. Right-click any of the selected files and choose Convert from the menu that opens.

    3. Select painted tlv from the File format drop down menu.

    4. Choose the saving location and, if you have selected one sequence, the frame range.

    5. Activate the Skip Existing Files to to prevent overwriting already existing files.

    6. Choose the folder where the unpainted files are located.

    7. Specify the Suffix used for namig the unpainted version of the files (default is _u, but you can use anything you like when preparing the files for convertion).

    8. Activate the Apply Autoclose.

    9. Choose how to manage Antialiasing fom the drop down menu. You can preserve the original antialiasing selecting Keep Original; add some antialiasing selecting Add and writing an Intensity value in the following text input field; remove the antialiasing selecting the Remove option and writing a Threshold value in the following text input field.

    10. Choose how to manage the palette of the tlv file/s you are going to create. By default a new palette is created. If you prefer to use an existing palette press the button next the palette field and use the browser to locate the palette file you desire to use.

    11. Click the Convert button.

.. tip:: **To convert files to the painted TLV format from non AA source:**

    1. Select the Raster Full color file you want to convert. 

    2. Choose the saving location and, if you have selected one sequence, the frame range.

    3. Activate the Skip Existing Files to to prevent overwriting already existing files.

    4. Choose the output folder.

    5. Activate the Apply Autoclose if needed.

    6. Choose how to manage the palette of the tlv file/s you are going to create. By default a new palette is created. If you prefer to use an existing palette press the button next the palette field and use the browser to locate the palette file you desire to use. Sets a Tolerance value for the correlation between the RGB value of the areas and the indexes color of the palette.

    7. Click the Convert button.

.. tip:: **To rename files:**

    1. Select the files you want to rename. 

    2. Right-click any of the selected files and choose Rename from the menu that opens.

    3. In the dialog that opens assign a new name to the file and choose whether to delete the original files by activating the related option.

    4. Click the Rename button.

.. tip:: **To premultiply full-color images:**

    1. Select the files you want to premultiply. 

    2. Right-click any of the selected files and choose Premultiply from the menu that opens.


.. _exposing_levels:

Exposing Levels
---------------
Animation levels, images for backgrounds and overlays, audio files, clips and other OpenToonz scenes, have to be exposed in the xsheet columns in order to be part of the scene.

If the level you want to use has already been loaded but not exposed, or it was removed from the scene, it can be retrieved from the Scene Cast window. 

In case you need to retrieve some specific drawings from an animation level, you can display it in the Level Strip, in order to select the drawings to expose.

.. note:: Animation levels you define directly in the scene, for instance levels you scanned, or drew directly in OpenToonz, are automatically exposed in the xsheet.


.. _using_the_scene_cast:

Using the Scene Cast
''''''''''''''''''''
All the animation levels you create or load in the scene are stored in the scene cast pane. Levels remain available in the scene cast even if they are not used in the scene anymore. From the scene cast, they can be exposed, edited, saved and removed. 




In the tree available on the left you can find the following:

- A clapboard icon referring to the current scene.

- The Cast folder containing all the animation levels you create or load.

- The Audio folder containing all the audio files you load or create (see  :ref:`Creating a Soundtrack <creating_a_soundtrack>`  ).

You can create new folders and sub-folders where animation levels can be arranged. The current location path in the cast tree is displayed in the cast top bar; folders can be renamed and new folders can be created. Levels can be displayed with related icons, or in a list displaying additional s that can be also used to sort files.

.. note:: Animation levels that are no longer available at the defined path can be identified by the red label.

.. tip:: **To display all the cast elements of a specific folder:**

    Click the folder icon in the cast tree on the left of the pane.

.. tip:: **To display all the cast elements:**

    Click the clapboard icon at the top of the cast tree on the left of the pane.

.. tip:: **To choose the cast display mode:**

    Do one of the following:

    - Click the icon button (|thumbnails|) in the bottom bar of the cast to display levels with the related icons.



    - Click the list button (|list|) in the bottom bar of the cast to display levels in a list; click the labels at the top of the  columns to sort files accordingly.

.. tip:: **To resize the scene cast sections:**

    Do any of the following:

    - Click and drag the separator to resize sections. 

    - Click and drag the separator towards the window border to hide a section.

    - Click and drag the separator collapsed to the window border towards the window center to display again the hidden section.

.. tip:: **To rename an existing folder:**

    Double-click the folder name and rename it.

.. tip:: **To create a new folder:**

    Click the new folder button (|new_folder|) in the bottom bar of the cast.



.. tip:: **To move one folder up in the cast tree:**

    Click the folder up button (|folder_up|) in the bottom bar of the cast.



.. tip:: **To perform a selection:**

    Do one of the following:

    - Click to select a level.

    - Ctrl-click (PC) or Cmd-click (Mac) to add a level to or remove it from the selection.

    - Shift-click to extend the selection.

.. tip:: **To move levels to a folder:**

    Select them and drag them to the folder in the cast tree.

.. tip:: **To expose the selection:**

    Do one of the following:

    - Choose Level > Expose in Xsheet.

    - Right-click the selection in the scene cast and choose Expose in Xsheet from the menu that opens. In case of a multiple level selection, each level will be placed in a different column, starting from the first empty one.

    - Drag and drop the selection to the xsheet cell where you want to start exposing it. In case of a multiple level selection, each level will be placed in a different column. 

.. tip:: **To display an animation level in the level strip:**

    Do one of the following:

    - Select it in the scene cast and choose Level > Display in Level Strip.

    - Right-click it in the scene cast and choose Display in Level Strip from the menu that opens.

.. tip:: **To remove the selected elements:**

    Right-click the selection in the scene cast and choose Remove Level from the menu that opens.

.. note:: Levels can be removed only if they are not used in the scene.

.. tip:: **To remove all the unused elements:**

    Do one of the following:

    - Choose Level > Remove All Unused Levels.

    - Right-click in the scene cast and choose Remove All Unused from the menu that opens.


.. _using_the_level_strip:

Using the Level Strip
'''''''''''''''''''''
When an animation level is displayed in the level strip, you can select the specific drawings you want to expose in the xsheet. This feature may prove useful especially when you need to retrieve some drawings that belongs to the level, but that are not available in the xsheet cells.

.. tip:: **To display an animation level in the level strip:**

    Do one of the following:

    - Select any level drawing exposed in the xsheet.

    - Select it in the scene cast and choose Level > Display in Level Strip.

    - Right-click it the scene cast and choose Display in Level Strip from the menu that opens.

.. tip:: **To select drawings in the level strip:**

    Do one of the following:

    - Click to select a drawing.

    - Ctrl-click (PC) or Cmd-click (Mac) to add a drawing to or remove it from the selection.

    - Shift-click to extend the selection.

.. tip:: **To expose the selection:**

    Do one of the following:

    - Copy and paste the selection in the xsheet into the cell you want.

    - Right-click in the level strip selection and choose Expose in Xsheet from the menu that opens. Drawings will be exposed at the beginning of the first empty column.

    - Drag and drop the selection to the xsheet cell where you want to start exposing it.

    - Drag and drop the selection to the xsheet cell where you want to start exposing it and keep the Shift key pressed, to insert them if other content is already exposed in the destination cells.

    - Drag and drop the selection to the xsheet cell where you want to start exposing it and keep the Alt key pressed, to overwrite any other content previously exposed in the destination cells.

.. note:: When it is not possible to release the selection, a red outline is displayed instead of the selection.


.. _replacing_levels:

Replacing Levels
''''''''''''''''
An animation level exposed in the xsheet can be easily replaced by another animation level, preserving any editing performed in the sequence of drawings exposed in the column cells. In this way it is possible to reuse the same edited sequence for different levels. For example you can reuse the edited sequence of a character level for the related shadow level by copying and pasting the character sequence, then replacing the character level with the shadow one.

It is possible to replace the level as a whole, or limited only to selected cells. In both cases only the content of the selected cells will be replaced: if any drawing of the replaced level is exposed somewhere else in the xsheet, it will not be affected by the replacing operation.

In case the new level does not contain some of the frames you are going to replace, the level name and number in the cell turn red to warn you that there is no drawing available for that cell.

The original level is preserved in the scene cast from where it can be retrieved, or removed (see  :ref:`Using the Scene Cast <using_the_scene_cast>`  ). 

.. tip:: **To replace a level in the xsheet:**

    1. Select the cells where the level you want to replace is exposed.

    2. Do one of the following:

    - Choose Level > Replace Level.

    - Right-click the selection and choose Replace Level from the menu that opens.

    3. In the browser select the new level, and click the OK button (see  :ref:`Using the File Browser <using_the_file_browser>`  ).


.. _editing_level_settings:

Editing Level Settings
----------------------
Once a level is exposed, its properties, like path, DPI and subsampling, can be controlled in the Level Settings dialog. Settings are the following:

- Name is the name used to identify the level, by default it is the same name of the file.

- Path displays the location of the file, using default folder aliases if needed. By typing in this field, or using the browser button, you can update the path to a different location, or to different file.

.. note:: If in the browser you choose any project default folder, in the path field the full path will be replace by the related default folder alias (see  :ref:`Project Default Folders <project_default_folders>`  ).

- Scan Path displays the location of the scanned images that were cleaned up to obtain the actual level (see  :ref:`Cleaning-up Scanned Drawings <cleaning-up_scanned_drawings>`  ). This is available only for Toonz raster levels.

- DPI lets you change the level DPI, thus changing its size. To return to the original image DPI set the option menu above to Image DPI. 

- Forced Squared Pixel forces a level that has a different horizontal and vertical DPI, and therefore is displayed stretched, to have the pixel shape squared, and thus to be displayed properly. 

 |Toonz71_243| 

    - Width and Height let you set a different size for the level, thus changing its DPI. The level maintains its A/R.

    - Use Camera DPI button applies to the level automatically the camera DPI. It is useful when the level has the same size of the camera but different DPI, and you want it to match perfectly the camera.

    - Information about Camera DPI, Image DPI and Image Resolution are displayed for reference.

    - Premultiply premultiplies the alpha channel of the level. Images which have a meaningful alpha channel come in two types: premultiplied or not. A non-premultiplied image can be recognized when it is loaded in OpenToonz because its edge, where there is a complete transparence on one side and opacity on the other, is not smooth, but displays a solid halo. With the premultiply operation it is possible to transform the image alpha-channel so that it is correctly displayed in OpenToonz camera stand, preview and rendering.

    - White As Transparent sets the pure white color (i.e. with red, green and blue values to 255) as transparent and automatically adds some antialiasing to the level images. This option is meant for animation levels generated from third-party software (such as Retas) that do not have a transparent background but a solid white one, and whose lines do not have antialiasing.

    - Add Antialiasing give to the user, if activated, the possibility to add antialiasing to levels. The antialias value have to be specified in the Antialias Softness field and range from 0 to 100. This option is available on Toonz Raster Levels and Raster Levels.

    - Subsampling sets the simplifying factor to be applied to animation levels, clips and images when displayed in the work area in order to have a faster visualization and playback; for example if it is 2, one pixel every two pixels is displayed. The default value is defined in Xsheet > Scene Settings where a value for Toonz raster levels and another for clips and full-color images can be defined.

.. note:: The subsampling factor can also be applied to all the animation levels exposed in selected columns by right-clicking the header of any selected column and choosing the related Subsampling command from the menu that opens.

.. tip:: **To open the Level Settings dialog:**

    Do one of the following:

    - Select a level in the xsheet and choose Level > Level Settings.

    - Right-click a level in the xsheet and choose Level Setting from the menu that opens.

    - Right-click a level in the cast and choose Level Setting from the menu that opens.


.. _working_with_xsheet_columns:

Working with Xsheet Columns
---------------------------
When levels are exposed in the xsheet, they are placed in columns. The column stacking order sets which drawings and images are placed on top, or behind, other images. Its direction is from left to right, so what is on the left is behind what is on the right. Use the shortcuts > and < to move between the columns.

The xsheet is divided into sections by horizontal markers, whose interval can be customized; at each marker the name of the level exposed in the xsheet is displayed.

Column cells may have different colors according to the type of level they contain. Toonz animation levels are displayed in light green; raster drawings, full color images, sequences and clips are displayed in light blue; sub-xsheet in light red (see  :ref:`Using Sub-xsheets <using_sub-xsheets>`  ); FX that create computer generated images in light orange (see  :ref:`Using the FX Schematic <using_the_fx_schematic>`  ); audio files in yellow (see  :ref:`Creating a Soundtrack <creating_a_soundtrack>`  ).

The column header contains information about the column content.

From the top you can see :

- A number representing the stacking order.

- A camera stand toggle (|camera_stand|) allowing you to hide, display, or display with a limited opacity the column content in the work area. When activated an animation table icon is visible in the toggle; the icon is greyed out in case a limited opacity is set.

- A render toggle (|preview|) allowing you to include or not the column content in the rendering; when activated an eye icon is visible in the toggle.

.. note:: The camera stand and the render toggles are linked to similar toggles available in the schematic column nodes (see  :ref:`Using the Stage Schematic <using_the_stage_schematic>`  and  :ref:`Using the FX Schematic <using_the_fx_schematic>`  ).

- A lock toggle (|lock|) allowing you to prevent any editing in the column; when activated a padlock icon is visible in the toggle.



    - An area where the name of the column is displayed, that by default is the name of the first exposed level. The area color indicates the type of level exposed in the column.

    - A preview icon of the first drawing or image exposed in the column.

.. note:: The icons on the xsheet column headers can either be displayed at once when the scene is opened, or on demand by clicking on the column header, according to the Column Icons option available in Xsheet > Scene Settings.

    - An area where the object and center to which the column is linked is displayed, that by default is Pegbar 2, center B (see  :ref:`Linking Objects <linking_objects>`  ).

The column on the far left displays the frame number, with the cursor indicating the current frame. The cursor can be used to set the current frame and allows you to activate the onion skin mode to better check the animation (see  :ref:`Using Onion Skin <using_onion_skin>`  ). 

.. note:: When the animation is played back, the xsheet scrolls according to the current frame cursor position in order to display the current frame. To disable the scrolling deactivate the Xsheet Autopan during Playback option available in the Preferences > Interface dialog.

At the top of the frame number column there are buttons for creating and navigating memos that can be posted in the xsheet (see  :ref:`Using Memos <using_memos>`  ).

The xsheet content can be scrolled to examine its content, while the header area and the frame column are always visible; in this way it's easier to understand how the scene is built.

Columns you want to hide in the xsheet can be also folded in order to save space in the interface. Once folded they can be unfold at any moment and be visible in their original position.

.. tip:: **To scroll the xsheet:**

    Do one of the following:

    - Middle-click and drag to scroll in any direction.

    - Use the mouse wheel to scroll up or down.

    - Use the scrolling bars to scroll only within the exposed section of the xsheet.

    - Use the Up Arrow and Down Arrow keys to move one frame up or down.

    - Use Shift+Up Arrow and Shift+Down Arrow keys to move to the previous or next drawing. Use this option if you want to skip the hold frames.

    - Use the Page Up and Page Down keys to scroll the visible frames up or down.

    - Use the Home and End keys to scroll up to the beginning or the end of the xsheet content.

.. tip:: **To set the marker interval:**

    1. Choose Xsheet > Scene Settings.

    2. In the dialog that opens use the Marker Interval to set the frame interval between two markers, and the Start Frame to set at which frame the first marker has to be displayed. 

.. tip:: **To name a column:**

    Double-click the column name in the header and type a new name.

.. tip:: **To link a column to an object:**

    1. Click the object name in the column header, and select a different object from the menu that opens. Only available columns and pegbars are displayed.

    2. Click the object center in the column header, and select a different center from the menu that opens (see  :ref:`Linking Objects <linking_objects>`  ).

.. tip:: **To select columns:**

    Do one of the following:

    - Click the column header to select a column.

    - Click and drag in the column icon to select contiguous columns.

    - Ctrl-click (PC) or Cmd-click (Mac) to add a column to or remove it from the selection.

    - Shift-click to extend the selection.

.. tip:: **To move a column selection:**

    Click any area displaying the name of column in the header, and drag it to the new position.

.. tip:: **To edit a column selection:**

    1. Select the columns you want to edit.

    2. Do one of the following:

    - Use the Copy command to keep in memory the selection for further operations.

    - Use the Cut command: to eliminate the selection from the scene and keep it in memory for further operations. The column elimination causes the following columns to shift left.

    - Use the Paste command to paste the selection kept in memory starting from the selected column. The command causes following columns to shift right.

    - Use the Delete command to delete the selection.

    - Use the Insert command to insert empty columns before the selection; inserted columns will be as many as the selected ones.

.. note:: All these commands are also available in the menu that opens when right-clicking the column header.

.. tip:: **To show or hide a column contents in the work area:**

    Do one of the following:

    - Click the camera stand toggle (|camera_stand|) on the upper right corner of the column header. The icon is greyed out in case a limited opacity is set (see below). If you right-click the toggle you can select commands from a menu that opens that lets you affect several columns at the same time.



    - Right-click the column content in the work area and choose the Hide or Show command related to the column you want to hide or show.

.. tip:: **To set a limited opacity for a column content:**

    Click and hold the camera stand toggle (|camera_stand|) on the upper right corner of the column header, and use the slider that is displayed to set the column opacity.



.. tip:: **To include or exclude a column contents from the rendering:**

    Click the render toggle (|preview|) on the upper right corner of the column header. If you right-click the toggle you can select commands from a menu that opens that let you affect several columns at the same time.



.. tip:: **To lock or unlock a column contents:**

    Click the lock toggle (|lock|) on the upper right corner of the column header (button on the right). If you right-click the toggle you can select commands from a menu that opens that let you lock or unlock several columns at the same time.



.. tip:: **To fold columns:**

    1. Select the columns you want to fold.

    2. Right-click the selection and choose Fold Columns from the menu that opens.

.. tip:: **To unfold columns:**

    Click the fold visible between the column headers.


.. _working_with_xsheet_cells:

Working with Xsheet Cells
-------------------------
When a level is exposed in a column, each cell contains a reference to a particular image. You may empty some cells, repeat some of them or change their order without affecting the real drawings sequence, because you are operating on references. This means that when a scene contains several cells referring to a drawing of an animation level, they all refer to the same drawing. This implies that when you modify a drawing of an animation level, all the cells in the xsheet referring to that drawing will consequently change their content.

.. note:: When the scene contains a reference to a drawing that is eliminated from the level, the drawing name and number in the cell turn red, to warn you that there is no drawing available for that cell anymore.

When you select a cell, you can work on the drawing it contains by using tools in the work area. 

When one or more cells are selected you can perform standard cut, copy, paste, delete and insert operations in the xsheet. In this case you are not modifying the animation level frames but simply changing the way it is exposed in the xsheet.

Selected cells can also be dragged to a new position in the xsheet, in duplicating, inserting or overwriting mode as well. When they are dragged to an empty column, it is possible to move along the data of the column, i.e. the movement and special FX, where they were originally exposed.

.. tip:: **To modify a drawing exposed in a cell:**

    1. Select the cell in the xsheet where the drawing is exposed.

    2. Use the tools to edit it in the work area. 

.. tip:: **To select several cells:**

    Do one of the following:

    - Click and drag to select a series of cells.

    - Shift-click a cell to extend the selection up to that cell.

    - Click the dark vertical strip available on the left of the cells, to select the continuous sequence of drawings belonging to the same animation level.

    - Press Ctrl and drag to include keys in the selection. A red frame will be shown around the selection.

.. tip:: **To edit cells with the Edit menu commands:**

    You can do the following:

    - Use the Copy command to keep in memory the selection for further operations.

    - Use the Cut command to eliminate the selection from the xsheet and keep it in memory for further operations. The cell elimination causes the following cells to shift up.

    - Use the Paste command to paste the selection kept in memory into the xsheet starting from the selected insertion cell. The command causes the following cells to shift down. 

    - Use the Delete command to empty the selected cells from any reference. 

    - Use the Insert command to insert blank cells before the selection; inserted cells will be as many as the selected ones. 

.. note:: All the Edit menu commands are also available in the menu that opens when right-clicking the xsheet cells.

.. tip:: **To edit cells with the Cells menu commands:**

    You can do the following:

    - Use the Reverse command to invert the order of the selected cells.

    - Use the Swing command to append the selected cells at the end of the selection in a reversed order. The last cell of the selection will not be repeated.

    - Use the Random command to rearrange the selected cells in a random order. The order changes every time you use the command.

    - Use the Autoexpose command to repeat the selected cells as if filling the numbering gap between two subsequent drawings. For example if the command is applied to two cells where drawing 2 and 5 are exposed, the result will be four cells with drawings 2, 2, 2 and 5. The command works only if the selection is increasingly numbered.

.. note:: If the Autoexpose command is used on an level numbered 1, 3, 5, 7, etc., the level will be automatically exposed step 2.

- Use the Repeat command to open a dialog that allows you to repeat cyclically the selected cells by specifying a number of times, or the frame number up to which the selection has to be repeated.

- Use the Reset Step command to remove any animation step in the selected cells, preserving the order of the exposed drawings.

- Use the Increase Step command to increase the animation step of the selected cells by one unit. 

- Use the Decrease Step command to decrease the animation step of the selected cells by one unit; if a drawing is exposed in one cell only, it will be preserved.

- Use the Step 2, Step 3 or Step 4 command to repeat the selected cells in order to have a step 2, step 3, or step 4 animation.

- Use the Each 2, Each 3 or Each 4 command to preserve only one cell each 2, each 3, or each 4 of the selection, and delete the others.

- Use the Roll Up command to shift the content of selected cells up, with the top cell content replacing the bottom cell one.

- Use the Roll Down to shift the content of selected cells down, with the bottom cell content replacing the top cell one.

.. note:: All the Cells menu commands are also available in the menu that opens when right-clicking the xsheet cells.

.. tip:: **To drag a cell selection:**

    Do one of the following:

    - Click the dark vertical strip available on the left of the cells, and drag them to move them to a new position. 

    - Ctrl-click (PC) or Cmd-click (Mac) the dark vertical strip available on the left of the cells, and drag them to the new position duplicating them.

    - Shift-click the dark vertical strip available on the left of the cells, and drag them to the new position inserting them if other content is exposed in the destination cells.

    - Alt-click the dark vertical strip available on the left of the cells, and drag them to the new position overwriting any other content previously exposed in the destination cells.

.. note:: When it is not possible to release the selection, a red outline is displayed instead of the selection.

.. tip:: **To drag a cell selection moving along the column data:**

    1. Choose File > Preferences > General.

    2. Set the Cell-dragging Behaviour option to Cells and Column Data.

.. note:: Column data are moved along only when dragging the selected cells to an empty column.

.. note:: The column data are moved along except for the linked columns, because linked columns can only have one parent column.


.. _using_the_smart_fill_handle:

Using the Smart Fill Handle
'''''''''''''''''''''''''''
The Fill Handle allows you to edit cells directly from within the xsheet. 

It is the small tab appearing at the bottom of the cell selection. By dragging this handle you can repeat a cell or a group of cells, you can add cells, or you can delete the last cells of a sequence. The behavior of the handle is smart: this means that the way cells are repeated, added, or deleted depends on the selection content.

.. note:: Editing cells with the Fill Handle makes the cells placed below the selection shift up or down.

.. tip:: **To edit cell content with the Fill Handle:**

    Do one of the following:

    - If you want to repeat a cell content for some frames, select the cell and drag the fill handle down.

    - If you want to lengthen a progressive sequence, select the cells where the sequence is exposed, and drag the fill handle down: sequence will be lengthen according to the progressive numbering. For example if the sequence is 1, 3, 5, the added images will be 7, 9, 11, etc. This works for any step the sequence may have.

    - If you want a random sequence to be repeated, select the sequence and drag the fill handle down: the sequence will be lengthened according to the sequence numbering. For example if the sequence is 3, 6, 4, 1, the added images will be 3, 6, 4, 1, 3, 6, etc.

    - If you want a progressive sequence to be repeated, first copy the sequence first drawing at the end of the sequence, then select all and drag down the fill handle. For example if the sequence is 1, 2, 3, 4, copy the drawing 1 at the end of the sequence (the result will be 1, 2, 3, 4, 1), and the added drawings will be 2, 3, 4, 1, 2, etc.

    - If you want to delete some cells, select a region so that the cells you want to delete are in the last rows, and drag the fill handle up.


.. _stretching_the_xsheet_timing:

Stretching the Xsheet Timing
''''''''''''''''''''''''''''
If you need to change the timing of a selection of cells, a selected frame range, or the whole xsheet, you can use the Time Stretch dialog. 

 |Toonz71_252| 

Options are the following.

- Stretch defines if the new timing has to be applied to the Selected Cells, the Selected Frame Range, or to the Whole Xsheet.

- Old Range displays the frame duration of the selection.

- New Range defines the new frame duration of the selection.

.. tip:: **To stretch the xsheet timing:**

    1. Select the cells, or define the frame range you want to stretch.

    2. Do one of the following:

    - Choose Cells > Time Stretch.

    - Right-click the selection and choose Time Stretch from the menu that opens.

    3. Define the time stretching options, then click the Stretch button.


.. _working_globally_with_frames:

Working Globally with Frames
----------------------------
It is possible to insert or delete frames affecting the xsheet as a whole, or a selection of xsheet columns. 

Inserting or deleting frames can be useful if you want to change the timing of the animation, for instance if you want to slow down or speed up an animation. 

When a frame is inserted, the current frame cells are duplicated, and all the following cells are shifted down. If some animation keys are defined for object transformations and FX parameters, they will be shifted down as well to keep the animation consistency (see  :ref:`Animating Objects <animating_objects>`  and  :ref:`Editing FX Settings <editing_fx_settings>`  ).

When a frame is removed, the current frame cells are deleted, and the following cells are shifted up. If some animation keys for object transformations and FX parameters are defined in the removed frame, they will be deleted and following keys will be shifted up (see  :ref:`Animating Objects <animating_objects>`  and  :ref:`Editing FX Settings <editing_fx_settings>`  ).

.. tip:: **To insert a frame:**

    1. Select the frame before which you want to insert a new frame.

    2. Choose Xsheet > Insert Frame.

.. tip:: **To remove a frame:**

    1. Select the frame you want to delete.

    2. Choose Xsheet > Remove Frame.


.. _using_sub-xsheets:

Using Sub-xsheets
-----------------
A sub-xsheet is a scene exposed in a single xsheet column. It can contain as many columns as you want, and other sub-xsheets as well. 

When it is opened, the sub-xsheet contents are displayed in the xsheet pane. When it is closed, it is displayed in the xsheet as a light red column, with the column icon displaying a render of its content. The column cells displays the name of the sub-xsheet, and the cell number is a reference to the frame of the sub-xsheet content, i.e. cell 4 is a reference to frame 4 of the sub-xsheet. 

The closed sub-xsheet column length depends on how many frames its content lasts at the time you create it, and it is not affected when you edit the sub-xsheet content.

Sub-xsheet columns can be animated like any other animation column, and FX can be assigned to it, affecting all the sub-xsheet content as a whole. 

Sub-xsheet column cells can be edited, for example to create a cycle, or cut, copied and pasted like any other exposed level (see  :ref:`Working with Xsheet Cells <working_with_xsheet_cells>`  ). Like any other level, if some editing is performed in its frames, all the cells in the main xsheet referring to that sub-xsheet frame will consequently change their content. In case you want to create a copy of a sub-xsheet that refers to the same animation level database but whose content can be edited independently, you can choose to clone it. 

If you want to reset the editing of a closed sub-xsheet, you can resequence it, by resetting it to the original length and order of its contents.

You can start a new sub-xsheet from a blank column, or you can load a scene previously created with OpenToonz as a level of the current scene. You can also collapse selected columns to form a new sub-xsheet to better manage the scene, for example you can collapse into a sub-xsheet all the columns used to define a character, or to explode the sub-xsheet to automatically bring all of its contents into the xsheet where it is exposed.

As sub-xsheets can be loaded and saved, they can also be used for importing or exporting sections of an xsheet from one scene to another. For example, if you create a scene where several levels compose a character (head, body, shadow, etc.), you can save it as an xsheet, and import it later in a different scene as a sub-xsheet.

When working in a sub-xsheet, by default only its contents are displayed in the work area. If you need to edit the sub-xsheet contents while looking at the whole scene contents, you can activate the Edit in Place mode. 

Like standard xsheets, sub-xsheets can also contain audio files to be used for synchronizing a soundtrack with the animation. However, audio files loaded in sub-xsheets are ignored when an output file supporting audio is rendered, because the possibility to edit the sub-xsheet columns frame order could make the resulting soundtrack inconsistent (see  :ref:`Creating a Soundtrack <creating_a_soundtrack>`  ).


.. _creating_sub-xsheets:

Creating Sub-xsheets
''''''''''''''''''''
Sub-xsheets are managed by Xsheet menu commands, and by icons located on the right of the menu bar. 

When a sub-xsheet has not been created yet, only a single xsheet icon is displayed, representing the main xsheet. As soon as you create a sub-xsheet, a new icon is added on the right of the first one. 

 |Toonz71_253| 

If you create a new sub-xsheet inside a sub-xsheet, another icon will be added, and so on. The icons are a reference that lets you understand in which level of the sub-xsheet hierarchy you are currently working: the icon on the far right is the current scene you are editing; icons on its left represent the different levels of the hierarchy.

You can also create a sub-xsheet by collapsing one or several columns where levels are exposed, choosing to include when needed the pegbars to which the columns are linked; or you can cut or copy columns and drawings outside of the sub-xsheet, then paste them inside it. 

.. note:: The main xsheet will share with its sub-xsheets the animation level database, so if the same level is loaded in the main xsheet and in one of its sub-xsheets, the level and its properties are shared.

When copying sub-xsheet columns and cells, their copies refer always to the same sub-xsheet contents: if changes are made in the sub-xsheet, all the cells in the main xsheet referring to that sub-xsheet will consequently change their content. If you want to create a copy of a sub-xsheet whose contents can be changed independently as concerning internal level exposure, object animation and applied FX, it is possible to clone it.

.. tip:: **To create a sub-xsheet from a blank column:**

    1. Select a blank column.

    2. Do one of the following to create the sub-xsheet:

    - Choose Xsheet > Open Sub-xsheet.

    - Click the arrow button on the right of the xsheet icon. 

    - Right-click the column header and choose Open Sub-xsheet from the menu that opens.

    3. Start editing the sub-xsheet: you can perform every operation you can do in a standard scene, such as load or create animation levels, or edit the camera, table, pegbars and the column position. You can see that you are working in a sub-xsheet because on the right of the menu bar a new xsheet icon is displayed: the one on the right represents the current sub-xsheet, the one on the left the main scene.

.. tip:: **To exit a sub-xsheet:**

    Do one of the following

    - Choose Xsheet > Close Sub-xsheet.

    - On the right of the menu bar, click the xsheet icon on the left of the icon representing the current xsheet. 

.. tip:: **To open a closed sub-xsheet:**

    1. Select the sub-xsheet column in the xsheet, or the sub-xsheet node in the schematic.

    2. Do one of the following:

    - Choose Xsheet > Open Sub-xsheet.

    - Click the arrow button on the right of the xsheet icons.

    - Right-click the column header and choose Open Sub-xsheet from the menu that opens.

.. tip:: **To create a sub-xsheet by collapsing one or several columns:**

    1. Select the columns you want to be part of the sub-xsheet in the xsheet or in the schematic.

    2. Do one of the following:

    - Choose Xsheet > Collapse.

    - Right-click any column header and choose Collapse from the menu that opens.

    3. Choose whether to include relevant pegbars in the sub-xsheet or collapse selected columns only, then click the OK button.

.. tip:: **To clone a sub-xsheet:**

    1. Select the sub-xsheet column where the sub-xsheet you want to clone is exposed.

    2. Do one of the following:

    - Choose Xsheet > Clone Sub-xsheet.

    - Right-click the column header and choose Clone Sub-xsheet from the menu that opens.

.. tip:: **To edit a sub-xsheet in its context:**

    Right-click the related xsheet icon on the right of the menu bar, and choose Enable Edit in Place from the menu that opens.

.. tip:: **To exit editing a sub-xsheet in its context:**

    Right-click the related xsheet icon on the right of the menu bar, and choose Disable Edit in Place from the menu that opens.

.. tip:: **To resequence a sub-xsheet:**

    1. Select the column containing the sub-xsheet.

    2. Do one of the following:

    - Choose Xsheet > Resequence.

    - Right-click the column header and choose Resequence from the menu that opens.


.. _loading_a_scene_as_a_sub-xsheet:

Loading a Scene as a Sub-xsheet
'''''''''''''''''''''''''''''''
Previously saved OpenToonz scenes can be loaded in a xsheet as sub-xsheets. 

Every time a scene is loaded as a sub-xsheet, its contents are imported into the current project database according to the project default folders, in the same way as it would be if every single level was imported (see  :ref:`Using the File Browser <using_the_file_browser>`  ). 

This allows you to create a library of basic animations that can be loaded and edited in other xsheets to create more complex animations without affecting the original files or drawings. Even when the same sub-xsheet is loaded twice, it is handled as if two different sub-xsheets were loaded, whose contents and levels can be edited separately.

To keep the database well-ordered you can also activate the Create Sub-folder when Importing Sub-xsheet option in the Preferences > Loading dialog, that will automatically create, in the project default folder, a folder named as the sub-xsheet you are importing where the levels from the sub-xsheet will be copied. 

Once a sub-xsheet is loaded, its levels are available in the scene cast in a sub-folder named as the scene you loaded.

On the occasion the camera settings of the scene you are loading as a sub-xsheet are different from those of your current scene, you will be prompted whether to keep the sub-xsheet original camera settings, or to apply the camera settings of the current scene to the sub-xsheet as well.

.. note:: If the scene you import contains a file whose name is the same of a file already existing in the destination default folder, you will prompted whether to keep the existing file, overwrite it with the new one, or rename it adding a suffix you can decide. In this way you can control if files you are importing were already imported previously, or manage files that share the same name. 

.. tip:: **To load a previously saved scene as a sub-xsheet:**

    Do one of the following:

    - Choose File > Load Level and use the browser to load a TNZ file.

    - Choose File > Load As Sub-xsheet and use the browser to load a TNZ file.

    - Use the OpenToonz standard browser to drag the scene icon to the scene cast pane, the xsheet or the work area.

    - In the file browser right-click the scene icon and select Load As Sub-xsheet in the menu that opens.

.. note:: OpenToonz scene files can also be loaded by dragging and dropping them from the Windows Explorer or Mac OS Finder to the scene cast, xsheet, or work area.


.. _exploding_sub-xsheets:

Exploding Sub-xsheets
'''''''''''''''''''''
Sub-xsheets can be exploded to automatically bring their content into the xsheet where they are exposed. When exploding a sub-xsheet it is possible to choose to bring to the main xsheet when needed the pegbars to which columns are linked. 

.. note:: When a sub-xsheet is exploded, its columns and the related FX nodes are displayed as a group in the FX schematic in order to better retrieve them (see  :ref:`Using the FX Schematic <using_the_fx_schematic>`  ).

.. note:: If special FX are applied to the sub-xsheet column, they will not be applied to the exploded columns, but the disconnected FX nodes will remain as reference in the FX schematic.

.. tip:: **To explode a sub-xsheet:**

    1. Select the sub-xsheet column in the xsheet or in the schematic.

    2. Do one of the following:

    - Choose Xsheet > Explode.

    - Right-click the sub-xsheet column header and choose Explode from the menu that opens.

    3. Choose whether to bring relevant pegbars to the main xsheet, or to bring columns only, then click the OK button.


.. _saving_a_sub-xsheet_as_a_scene:

Saving a Sub-xsheet as a Scene
''''''''''''''''''''''''''''''
The content of a sub-xsheet can be saved as a standard scene, i.e. a TNZ file, in order to be loaded as a stand-alone scene or to be available for reuse in other scenes.

The sub-xsheet content will be saved according to the current project settings for default folders, as if you were saving a scene file (see  :ref:`Project Default Folders <project_default_folders>`  ).

.. tip:: **To save a sub-xsheet as a scene:**

    1. Open the sub-xsheet you want to save, so that its contents are displayed in the xsheet.

    2. Choose Xsheet > Save Sub-xsheet As and use the browser to save the scene file (see  :ref:`Saving and Loading Scenes <saving_and_loading_scenes>`  ).


.. _creating_a_soundtrack:

Creating a Soundtrack
---------------------
Audio clips can be loaded and edited in order to create a soundtrack for the scene; supported file formats are non-compressed ``WAV`` and ``AIFF``  files at 8 and 16 bit. There is no limit to the number of audio clips that can be loaded in a scene.

To load an audio clip you can use the browser room; if an audio clip is imported, it is saved in the +extras folder (see  :ref:`Using the File Browser <using_the_file_browser>`  ). Loaded audio clips are also stored in the Audio folder of the scene cast.

Each loaded audio clip is exposed in a different xsheet column as a series of visible sound waves to make the editing job easier; the number of frames it occupies depends on the length of the audio file and the frame rate set for the current scene. For example an audio clip 3 seconds long, imported into a scene whose frame rate is 12, will occupy 36 frames; if imported in a scene whose frame rate is 24 will occupy 72 frames (see  :ref:`Setting the Frame Rate <setting_the_frame_rate>`  ). 

 |Toonz71_254| 

Audio columns can be edited the way you edit any other column. The column header contains information about the column content. From the top you can see:

- A number representing the stacking order, that is not relevant for audio columns.

- A camera stand toggle (|camera_stand|) allowing you to include or not the column content when scrubbing the audio with the current frame cursor (see below); when activated an animation table icon is visible in the toggle.



- A render toggle (|preview|) allowing you to include or not the audio column content in the rendering; when activated an eye icon is visible in the toggle.

- A lock toggle (|lock|) allowing you to prevent any editing in the column; when activated a padlock icon is visible in the toggle.

- A vertical slider allowing you to set the volume.

- A loudspeaker icon that lets you play the contents back.

The Level Settings dialog is available for audio clips as well, allowing you to check the location of the related file, or to update the loading path to a different location, or to a different file (see  :ref:`Editing Level Settings <editing_level_settings>`  ).

The soundtrack you define with audio clips will be created by merging all of the contents of audio columns according to the volume you set for each of them. While it cannot be played back when using the playback controls in the viewer, it can be scrubbed with the current frame cursor in the xsheet frame column or in the viewer framebar, and played back when a scene is previewed (see  :ref:`Editing Audio Clips <editing_audio_clips>`  and  :ref:`Previewing the Animation <previewing_the_animation>`  ). 

When a scene is rendered in a file format supporting audio, (MP4, MOV, WebM or AVI), the soundtrack will be included in the file (see  :ref:`Rendering the Animation <rendering_the_animation>`  ). 

.. note:: Audio clips loaded in sub-xsheets will not be included in the output soundtrack (see  :ref:`Using Sub-xsheets <using_sub-xsheets>`  ).

.. note:: As the soundtrack cannot be played back when viewing files in the OpenToonz flipbook, you can activate the Use Default Viewer for Movie Formats option in the Preferences > General dialog in order to view files with their own default viewer, e.g. QuickTime for the MOV format, thus playing back the soundtrack as well.

.. tip:: **To play the contents of an audio column back:**

    Click the loudspeaker icon available in the header of the column. Click it again to interrupt the playback.

.. tip:: **To set the volume of an audio column:**

    Use the vertical slider available in the column header.

.. tip:: **To include or exclude an audio when scrubbing the audio with the current frame cursor**

    Click the camera stand toggle (|camera_stand|) on the upper right corner of the column header. If you right-click the toggle you can select commands from a menu that opens that let you affect several columns at the same time.



.. tip:: **To include or exclude the audio column contents from the rendering:**

    Click the render toggle (|preview|) on the upper right corner of the column header. If you right-click the toggle you can select commands from a menu that opens that let you affect several columns at the same time.



.. tip:: **To lock or unlock a column contents:**

    Click the lock toggle (|lock|) on the upper right corner of the column header (button on the right). If you right-click the toggle you can select commands from a menu that opens that let you lock or unlock several columns at the same time.



.. _editing_audio_clips:

Editing Audio Clips
'''''''''''''''''''
Once loaded, audio clips can be moved up and down in the column, or to a different column, in order to be played starting from a certain frame of the animation. They can be trimmed to select a part of the whole clip and edited, by deleting or copying some sections, using standard edit commands the same way you use them on standard columns.

When a clip is trimmed, the trimmed part is not eliminated, but hidden, and it has a colored horizontal marker at its starting or ending, according to where it was trimmed: it is possible to retrieve the trimmed part by moving back the markers.

When a clip is split into sections by deleting, cutting or moving operations, it is automatically duplicated and trimmed to create the right result.

.. note:: Audio clips can be moved and pasted only to empty columns, or to other audio columns.

.. note:: All the editing does not affect the file on disk, as it refers only to the way the clip is used in the scene.

To find a particular section in an audio file, you can examine it by scrubbing it with the current frame cursor, either in the xsheet frame column or in the viewer framebar, or by selecting any section and automatically playing it back together with the animation. This allows you to easily spot and excerpt the sections you need from an audio file. 

.. tip:: **To select audio clips:**

    Do one of the following:

    - Click and drag to select a section of the clip.

    - Shift-click a clip cell to extend the selection up to that cell.

    - Click the dark vertical strip available on the left of the clip, to select the whole clip.

.. tip:: **To edit audio clips with the Edit menu commands:**

    You can do the following:

    - Use the Copy command to keep in memory the selection for further operations.

    - Use the Cut command to eliminate the selection from the xsheet and keep it in memory for further operations. The cell elimination causes the following cells to shift up.

    - Use the Paste command to paste the selection kept in memory in the xsheet starting from the selected insertion cell. The command causes the following cells to shift down. 

    - Use the Delete command to empty the selected cells from any reference. 

    - Use the Insert command to insert blank cells before the selection; inserted cells will be as many as the selected ones. 

.. note:: All the Edit menu commands are also available in the menu that opens when right-clicking the xsheet cells.

.. tip:: **To move a clip selection:**

    Do one of the following:

    - Click the dark vertical strip available on the left of the clip cells, and drag them to move them to a new position. 

    - Ctrl-click (PC) or Cmd-click (Mac) the dark vertical strip available on the left of the clip cells, and drag them to the new position duplicating them.

    - Shift-click the dark vertical strip available on the left of the clip cells, and drag them to the new position inserting them if other audio clips are loaded in the destination cells.

    - Alt-click the dark vertical strip available on the left of the clip cells, and drag them to the new position overwriting any other audio clips previously loaded in the destination cells.

.. note:: When it is not possible to release the selection, a red outline is displayed instead of the selection.

.. tip:: **To trim an audio clip:**

    Do any of the following:

    - Click and drag the starting of a clip to trim its starting part.

    - Click and drag the ending of a clip to trim its ending part.

    - Click and drag the marker of a trimmed clip to redefine the trimmed part.

.. tip:: **To scrub audio clips:**

    Do one of the following:

    - Drag the xsheet frame cursor up or down to scrub all the audio columns whose Camera Stand toggle is active.

    - Drag the frame cursor in the viewer framebar to scrub all the audio columns whose Camera Stand toggle is active.

    - Windows only: click and drag on the dashed vertical strip available on the right of the audio column cells: the selected section will be automatically played back.


.. _lip_synching:

Lip Synching
''''''''''''
When you need to synchronize the movement of a character’s lips with the sound of the speech, you can take advantage of the possibility to examine the audio files loaded in the scene.

Once you have created different mouth images, you can analyze the audio files to find where to place specific mouth drawings. If mouth drawings belong to one single animation level, you can quickly change the mouth drawing at a specific frame by picking drawings from the level strip or by flipping through drawings using one of the Skeleton tool (|skeleton|) features (see :ref:`Using the Level Strip <using_the_level_strip>`  and :ref:`Animating Models <animating_models>`  ).



The breakdown of audio files can be done by looking at the sound wave in the scene column, for example to spot where each word starts; by scrubbing the loaded audio clips with the current frame cursor either in the xsheet frame column or in the viewer framebar; and by listening to specific sections of the audio files.

When mouth images are placed in the proper place, you can check the sync by scrubbing or selecting again the audio file section you are interested in, because while listening to the selected audio section, the viewer will display the related animation frames.

This technique can be used in any case you need the sound to be perfectly synchronized with the action, for example a character playing an instrument, or a scene based on the rhythm of a music.

.. tip:: **To scrub audio clips:**

    Do one of the following:

    - Drag the xsheet frame cursor up or down to scrub all the audio columns whose Camera Stand toggle is active.

    - Drag the frame cursor in the viewer framebar to scrub all the audio columns whose Camera Stand toggle is active.

    - Windows only: click and drag on the dashed vertical strip available on the right of the audio column cells: the selected section will be automatically played back.

.. tip:: **To flip through the mouth drawings:**

    1. Do one of the following:

    - Select in the xsheet the animation level containing the mouth drawings.

    - Right-click in the work area on the mouth drawing you want to flip through, and choose the Select command related to the column containing the drawing you clicked.

    2. Choose the Skeleton tool (|skeleton|) and set the tool mode to Animate.

    3. In the work area click the label with the level name on the right of the current section pivot point and flip through following and previous frames by doing one of the following:

    - Drag up or down.

    - Click the up or down arrowheads.


.. _importing_magpie_files:

Importing Magpie Files
''''''''''''''''''''''
 |Toonz71_263| 

For lip synching it is possible to import into the xsheet TLS (i.e. Toonz Lip Sync) files exported from Magpie, a professional lip-sync and animation timing tool. 

While Magpie takes care of the audio file analysis and phoneme recognition, the import into OpenToonz allows you to assign a frame from an animation level to each phoneme, and automatically expose the result in an xsheet column; another column displaying the speech text as recognized in Magpie is created for reference.

.. tip:: **To export the OpenToonz lip sync file in Magpie:**

    1. Copy the file ``export-toonz.lua``  available in ``OpenToonz_stuff\config``  folder into the ``C:\Program Files (x86)\Third Wish Software & Animation\Magpie Pro\Scripts\Export``  folder.

    2. In Magpie choose File > Export and choose Toonz among the 2D software list to export the TLS file.

.. tip:: **To import a Magpie file:**

    1. Choose File > Import Magpie File.

    2. In the browser that opens retrieve the TLS file you exported from Magpie and click the Load button.

    3. In the dialog that opens choose the following:

    - Use Frame Range to define which section of the Magpie file you want to use to create the lip sync column in the xsheet.

    - Use the Animation Level section to retrieve the animation level you want to expose in the xsheet, and to specify which frame of the level has to be assigned to each phoneme; you can also use the viewer available at the bottom of the dialog to examine the frame of the selected animation level.

    4. Click the Import button.


.. _using_memos:

Using Memos
-----------
Memos can be posted in the xsheet at specific positions in order to add notes and comments to the scene. 

When editing a memo its color can be set, and the text you write can be formatted. Once posted, memos display the first letters of their content in order to be identified, and can be retrieved in the xsheet by navigating them.




.. tip:: **To post a memo:**

    1. Click the new memo button at the top of the frame number column.

    2. Type the text in the window that opens, format it and choose the memo color (see below) then click the Post button: the memo is posted at the current frame in the current column.

    3. Click and drag the posted memo to change its position.

.. tip:: **To format the text in the memo:**

    1. Select the text you want to format.

    2. Click the arrow that is displayed on the right of the selection to open the text toolbar.

    3. Choose the font family, size, color, style and paragraph alignment by clicking on the relevant menu and buttons in the toolbar.

.. tip:: **To change the memo color:**

    Choose a color in the palette available at the bottom of the open memo; palette colors can also be selected and edited by using the style editor.

.. tip:: **To navigate the memos posted in the xsheet:**

    Click the arrow buttons under the new memo button to check the previous or next memo: the xsheet automatically pans to show where the memo is posted.

.. tip:: **To open a memo:**

    Do one of the following:

    - Double-click it.

    - Right-click it and choose Open Memo from the menu that opens.

.. tip:: **To delete a memo:**

    Do one of the following:

    - Open it and click the Discard button.

    - Right-click it and choose Delete Memo from the menu that opens.


.. _saving_and_loading_scenes:

Saving and Loading Scenes
-------------------------
When working on a new scene the default name (untitled) followed by a progressive number is assigned to the scene until you save it with a different name. This name is also used in case the $scenepath variable is used in the project settings to store temporarily the material used in the scene.

.. note:: Untitled scenes and related material are stored in the ``OpenToonz_stuff\projects\temp``  folder, and deleted when the scene is saved with a proper name or not saved at all. Check regularly the ``temp``  folder, and if there is some content, delete it to free disk space.

Scene files can be saved and loaded as TNZ files using the related menu commands. Scenes have to be saved in the current project +scenes folder, or any of its sub-folders, in order to retrieve all the material when they are loaded back.

When you use the Save As command, if the $scenepath is used in the default folders definition, all the material used in the scenes and located in project default folders will be duplicated in folders related to the new scene (see  :ref:`Using the $scenepath Variable in Folder Definition <using_the_$scenepath_variable_in_folder_definition>`  ).

An option to automatically save the scene every given number of minutes is available in the Preferences > General dialog. If the option is activated, during the saving operation a message is displayed to notify the process.

.. note:: An asterisk after the scene name in the viewer and xsheet title bars denotes that there are unsaved changes for the current scene.

.. tip:: **To work on a new scene:**

    Choose File > New Scene.

.. tip:: **To save a scene:**

    Choose File > Save Scene.

.. tip:: **To save the current scene with a different name:**

    1. Choose File > Save Scene As.

    2. In the browser that opens select the current project +scenes folder, or any of its sub-folders, where you want to save the scene.

    3. Assign a name to the scene and click the Save button.

.. tip:: **To load a scene from the Load Scene browser:**

    1. Choose File > Load Scene.

    2. In the browser that opens retrieve in the +scenes folder of the current project, or any of its sub-folders, the scene you want to load and click the Load button.

.. tip:: **To load a scene from the OpenToonz standard browser:**

    Do one of the following:

    - Right-click the scene icon and choose Load Scene from the menu that opens.

    - Drag and drop the scene icon to the clapboard icon in the scene cast pane. 

.. note:: Scenes can also be loaded by dragging and dropping them from the Windows Explorer or Mac OS Finder to the clapboard icon in the scene cast.

.. tip:: **To load back a recently loaded scene:**

    Choose File > Open Recent Scene File, then select the scene you want to load from the available submenu.

.. tip:: **To revert the current scene to the last saved version:**

    Choose File > Revert Scene.

.. tip:: **To automatically save a scene every given number of minutes:**

    1. Choose File > Preferences > General.

    2. Activate the Save Automatically Every Minutes option and enter the number of minutes that have to pass between each saving operation.


.. _importing_and_exporting_scenes:

Importing and Exporting Scenes
------------------------------
In OpenToonz each scene file belongs to a specific project, so that the material created and used in the scene is located and can be retrieved from the project default folders.

If you need to copy the scene and the related material to a different project, it is possible either to import any scene file in the current project, or to export it to any other project available in the projectroot (see  :ref:`Setting up Projects <setting_up_projects>`  ).


.. _importing_scenes_from_a_different_project:

Importing Scenes from a Different Project
'''''''''''''''''''''''''''''''''''''''''
When trying to load a scene created in a different project, or not located in the current project +scenes folder or any of its sub-folders, you are prompted to decide whether you want to import the scene or change the current project (see  :ref:`Setting up Projects <setting_up_projects>`  ).

If you decide to import the scene, the scene will be loaded, and all the scene material will be imported in the following way:

- All the files that were located in the original project default folders (i.e. the ones loaded in the scene by using relative paths) will be copied into the related default folders of the current project (see  :ref:`Project Default Folders <project_default_folders>`  ).

- All the files that were located in external folders (i.e. the ones loaded in the scene by using absolute paths), will remain where they are.

While the material is automatically imported and saved in the current project, the scene file will not be saved until you will save it by using the Save Scene or Save Scene As commands.

It is also possible to import one or several scenes into the current project with no need to load and save them by using the Import Scene command.

In this case both the material files located in the original project default folders and the scene file will be copied in the related default folders of the current project.

.. note:: If the scene you import contains a file whose name is the same as a file already existing in the destination default folder, you will prompted whether to keep the existing file, overwrite it with the new one, or rename it adding a suffix you can decide. In this way you can control if files you are importing were already imported previously, or manage files that share the same name. 

.. tip:: **To load and import a scene from a different project:**

    1. Load the scene you want to import by using the Load Scene browser or the OpenToonz standard browser.

    2. Choose Import Scene in the dialog that opens: the scene is loaded and the related files will be copied into the default folders of the current project.

    3. Save the scene file in the current project +scenes folder

.. tip:: **To import one or several scenes from a different project without loading them:**

    1. Select the scenes you want to import in the OpenToonz standard browser.

    2. Right-click the selection and choose Import Scene from the menu that opens: the scene and the related material files copied in the default folders of the current project.


.. _exporting_scenes_to_a_different_project:

Exporting Scenes to a Different Project
'''''''''''''''''''''''''''''''''''''''
Scenes can be exported if you need either to copy them from a project to any other existing project, or to copy them to a new project that can be automatically created according to the current project settings.

In both cases the scenes files and the related assets will be automatically collected and copied in the related default folders of the destination project (see  :ref:`Collecting Assets <collecting_assets>`  ). 

 |Toonz71_265| 

.. note:: If the scene you export contains any file whose name is the same of a file already existing in the destination default folder, you will prompted whether to keep the existing file, overwrite it with the new one, or rename it adding a suffix you can decide. In this way you can control if files you are exporting were already exported previously, or manage files that share the same name. 

.. tip:: **To export one or several scenes to a different project:**

    1. Select the scenes you want to export in the OpenToonz standard browser.

    2. Right-click the selection and choose Export Scene from the menu that opens: the Export Scene dialog opens.

    3. In the dialog do one of the following:

    - Choose the Choose Existing Project option if you want to export the selected scenes to an existing project, and navigate the folder tree to choose the destination project. 

    - Choose the Create New Project option if you want to export the selected scenes to a new project based on the current one, and assign a name to the new project.

    4. Click the Export button.


.. _collecting_assets:

Collecting Assets
'''''''''''''''''
Files used in a scene can be located in the default folders of the current project, or loaded from an external folder (see  :ref:`Project Default Folders <project_default_folders>`  and  :ref:`Using the File Browser <using_the_file_browser>`  ). 

This means that when a project has to change location for any reason (e.g. for a backup), moving all the default folders does not grant that all the files required for the project scenes are moved along, because files loaded from external folders will remain where they are.

For this reason it is possible to collect all the files used in a scene, thus importing automatically in the project default folders all the files that were not imported at loading time. At the same time the scene file for which you are collecting assets will be automatically updated in order to correct all the loading paths of the newly imported files and keep consistency.

.. tip:: **To collect the assets of one or several scenes:**

    1. Select the scenes for which you want to collect assets.

    2. Right-click the selection and choose Collect Assets from the menu that opens: all the scene files that were located in external folders are copied into the default folders of the project, and the related paths used in the scene files are updated.


.. _scene_backup_files:

Scene Backup Files
''''''''''''''''''
When scenes are saved, backup files of previous versions are automatically stored in a folder named as the scene, that is located in ``+scenes\backups``  of the current project. 

The four previous scene versions are retained, and they are named as the scene with a progressive backup number: the highest the number, the more recent the backup.

For example if you have saved seven times the scene named my_scene, four backup versions of the scene named ``my_scene_3`` , ``my_scene_4`` , ``my_scene_5``  and ``my_scene_6``  are available in the ``+scenes\backups\my_scene`` folder.

If you want to recover a scene backup version of a scene, you have to remove the backup number so to have the correct scene name, and move the file into the +scenes folder.

.. tip:: **To recover a backup version of a scene:**

    1. Retrieve in ``+scenes\backups``  the folder named as the scene whose backup you want to recover.

    2. In the folder, retrieve the TNZ file related to the latest backup you want to recover, and rename it removing the backup number so to have the correct scene name.

    3. Copy and paste it into the +scenes folder, to replace the version you want to scratch.


.. _printing_xsheets:

Printing Xsheets
----------------
An xsheet can be saved as HTML file in order to view it on any computer by using an Internet browser, and to print it on paper.

The HTML file contains a header with general information, several tables, whose length and width you can decide, representing the xsheet with exposed levels and objects movements, and a list of the levels exposed in the xsheet with the related location on disk. 

If any sub-xsheets are used in the scene, they are displayed after the main xsheet where they are exposed.

The information displayed in the header and the appearance of the HTML table can be set by editing the following files located in the folder ``OpenToonz_stuff\profiles\layouts\settings`` :

- ``xsheet_html.xml``  contains the information used for the HTML xsheet header, and the size for the tables used to represent the xsheet content.

- ``xsheet.css``  is a Cascading Style Sheet file that is used to define the colors, layout, and other aspects of the HTML xsheet file (see below ).

When using the Print Xsheet command, a dialog with information about the location and name of the generated HTML file is displayed; then the generated HTML file is displayed in your default browser.

The HTML file is saved in the same location of the TNZ file; the CSS file used for its formatting is generated as well, by copying the one located in the folder ``OpenToonz_stuff\profiles\layouts\settings`` . If a CSS file is already available in the location where the HTML xsheet file is saved, it will be used instead of generating a new one.

.. note:: If you want to move the HTML xsheet file, you should move the CSS file as well, in order to preserve the HTML file appearance as defined by the CSS file.


.. _editing_the_html_xsheet_header_and_table_size:

Editing the HTML Xsheet Header and Table Size
'''''''''''''''''''''''''''''''''''''''''''''
The HTML xsheet header and the size for the tables used to represent the xsheet content can be defined by editing the`` xsheet_html.xml``  file available in the folder ``OpenToonz_stuff\profiles\layouts\settings`` . It can be edited with any text editor software, e.g. Notepad or TextEdit.

The whole text is included in the tag ``xsheet_html`` , that contains the elements ``page``  and ``info`` , where the different users and roles are defined. The basic structure of the file is the following:



::

    <xsheet_html>	<page rows="50">	<page columns="10">	<info name="Company" value="Company name"/>	<info name="Name" value="Value"/></xsheet_html>

By editing the ``page row``  and ``page columns``  values you can set the size of the table used for splitting the xsheet in sections. The size of the table allows you to fit each xsheet section to the paper size you want to use to print the xsheet on paper.

The ``info``  lines allows you to set information to be displayed in the header, for example the production name.

In the example file you can find the following lines:



::

    <info name="Company" value="Company name"/><info name="Name" value="Value"/>

These lines can be edited, and new lines, with the same syntax, can be appended, to provide all the information you want to appear in the header of the HTML xsheet file.

.. note:: By default the header contains the Project and Scene names and the number of frames the scene consists of; this information cannot be edited, as they are retrieved automatically from the scene file.

.. note:: The ``xsheet_html.xml``  file has to be well-formed, and so it can not contain an opening tag without its related closing tag, otherwise OpenToonz will not run. If you decide to edit the ``xsheet_html.xml``  file, make a backup copy first in case you need to revert the file to the original version.

.. tip:: **To edit the xsheet_html.xml file:**

    Open the ``xsheet_html.xml``  file available in the folder ``OpenToonz_stuff\profiles\layouts\settings`` with a text editor application (e.g. Notepad or TextEdit).

.. tip:: **To change the size of the table used for splitting the xsheet in sections:**

    Change the ``page row``  and ``page columns``  values in the ``xsheet_html.xml``  file.

.. tip:: **To edit the information displayed in the header:**

    Edit the ``info``  lines available in the ``xsheet_html.xml``  file, and append new ones if needed.

.. tip:: **To check if the xsheet_html.xml file is well-formed:**

    Open it with an Internet browser and check if all the elements are displayed in a nested list where they can be opened and closed to display or hide the related contents.


.. _editing_html_xsheet_appearance:

Editing HTML Xsheet Appearance
''''''''''''''''''''''''''''''
The HTML xsheet appearance can be defined by editing thexsheet.css file available in the folder ``OpenToonz_stuff\profiles\layouts\settings`` . 

The ``xsheet.css``  is a Cascading Style Sheet file that is used to define the colors, layout, and other aspects of the HTML xsheet file. It can be edited with any text editor software, e.g. Notepad or TextEdit. 

Editing the CSS file requires some skill in the CSS language, but some changes like table ruling thickness, or cell colors, can be easily done by expressing the thickness in pixels and colors as an RGB triplet in hexadecimal format.

Elements defined in the CSS are the following:

- ``header``  refers to the table used as header in the HTML xsheet file.

- ``table``  refers to the table used for displaying the xsheet sections.

- ``TH``  refers to the header cells of the tables. 

- ``first_numeric``  refers to the first numerical column of the xsheet tables.

- ``fxcell``  refers to the table cells belonging to special FX columns.

- ``subxsheetcell``  refers to the table cells belonging to sub-xsheet columns.

- ``TD``  refers to the generic table cells.

- ``TH.frame``  refers to the frame column

- ``TD.levelcell``  refers to the table cells belonging to standard level columns.

.. note:: The CSS files have to be written according to a specific syntax. If you decide to edit the ``xsheet.css``  file, make a backup copy first in case you need to revert the file to the original version.

.. tip:: **To edit the xsheet.css file:**

    Open the ``xsheet.css``  file available in the folder ``OpenToonz_stuff\profiles\layouts\settings``  with a text editor application (e.g. Notepad or TextEdit).


.. |Toonz71_233| image:: /_static/Toonz71/Toonz71_233.gif
.. |Toonz71_243| image:: /_static/Toonz71/Toonz71_243.gif
.. |Toonz71_252| image:: /_static/Toonz71/Toonz71_252.gif
.. |Toonz71_253| image:: /_static/Toonz71/Toonz71_253.gif
.. |Toonz71_254| image:: /_static/Toonz71/Toonz71_254.gif
.. |Toonz71_263| image:: /_static/Toonz71/Toonz71_263.gif
.. |Toonz71_265| image:: /_static/Toonz71/Toonz71_265.gif
.. |animate| image:: /_static/xsheet/animate.png
.. |skeleton| image:: /_static/xsheet/skeleton.png
.. |3d| image:: /_static/xsheet/3d.png
.. |camera_stand| image:: /_static/xsheet/camera_stand.png
.. |camera_view| image:: /_static/xsheet/camera_view.png
.. |folder_up| image:: /_static/xsheet/folder_up.png
.. |freeze| image:: /_static/xsheet/freeze.png
.. |list| image:: /_static/xsheet/list.png
.. |lock| image:: /_static/xsheet/lock.png
.. |new_folder| image:: /_static/xsheet/new_folder.png
.. |preview| image:: /_static/xsheet/preview.png
.. |thumbnails| image:: /_static/xsheet/thumbnails.png
