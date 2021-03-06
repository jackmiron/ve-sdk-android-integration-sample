# Banuba VideoEditor SDK
## Alert Dialog styles

There are following types of user notification used in Banuba Video Editor SDK:
- toast
- wait dialog (represents long running tasks)
- alert with control buttons

All of them are customized by theme attributes described in this file.

- [toastStyle](https://github.com/Banuba/ve-sdk-android-integration-sample/blob/main/app/src/main/res/values/themes.xml#L198)

    style to customize toast messages

    ![img](screenshots/alert1.png)

- [throbberViewStyle](https://github.com/Banuba/ve-sdk-android-integration-sample/blob/main/app/src/main/res/values/themes.xml#L42)

    style for the circle progress bar. It is allowed to customize gradient colors using custom attribute

- [waitDialogTextStyle](https://github.com/Banuba/ve-sdk-android-integration-sample/blob/main/app/src/main/res/values/themes.xml#L43)

    style for the TextView that shows a description

- [wait_dialog_throbber_bg](https://github.com/Banuba/ve-sdk-android-integration-sample/blob/main/app/src/main/res/values/themes.xml#L199)

    theme attribut that configures the background of circle progress bar within progress dialog

    ![img](screenshots/alert2.png)

Recently to customize alert dialogs with control buttons you should override fragment_dialog_alert.xml file in layout resource folder. For correct implemetation all views' ids should be the same as in the original file:

- alertTitleText - for dialog description
- alertPositiveButton - for the button meaning positive answer from the user (right button)
- alertNegativeButton - for the button meaning negative answer from the user (left button)

After overriding layout file you can use your any of your own styles to customize these views.

![img](screenshots/alert3.png)

Every alert dialog has its own type within SDK. It allows to customize descriptions and text over the positive and negative buttons. To do so you need to override the following string resources (they named according to the type of alert where they are used):
- "alert_delete_video_message"
    
    "alert_delete_video_positive"

    "alert_delete_video_negative"
- "alert_save_video_chunk_message"

    "alert_save_video_positive"

    "alert_save_video_negative"
- "alert_return_to_editor"

    "alert_return_to_editor_positive"

    "alert_return_to_editor_negative"
- "alert_return_to_trimmer"

    "alert_return_to_trimmer_positive"

    "alert_return_to_trimmer_negative"
- "alert_reset_all_message"

    "alert_reset_all_positive"

    "alert_reset_all_negative"
- "editor_alert_reset_all"

    "editor_alert_reset_all_positive"

    "editor_alert_reset_all_negative"
- "editor_alert_reset_effects"

    "editor_alert_reset_effects_positive"

    "editor_alert_reset_effects_negative"
- "editor_alert_delete_voice_record"

    "editor_alert_delete_voice_record_positive"

    "editor_alert_delete_voice_record_negative"


Also there is a possibility to add custom icon for every alert dialog type. To setup drawables for this reason they should be passed into custom theme attributes:

- [alert_camera_delete_video](https://github.com/Banuba/ve-sdk-android-integration-sample/blob/main/app/src/main/res/values/themes.xml#L50)
- [alert_camera_return_to_editor](https://github.com/Banuba/ve-sdk-android-integration-sample/blob/main/app/src/main/res/values/themes.xml#L51)
- [alert_camera_return_to_trimmer](https://github.com/Banuba/ve-sdk-android-integration-sample/blob/main/app/src/main/res/values/themes.xml#L52)
- [alert_camera_save](https://github.com/Banuba/ve-sdk-android-integration-sample/blob/main/app/src/main/res/values/themes.xml#L53)
- [alert_camera_reset_all](https://github.com/Banuba/ve-sdk-android-integration-sample/blob/main/app/src/main/res/values/themes.xml#L54)
- [alert_editor_delete_voice_record](https://github.com/Banuba/ve-sdk-android-integration-sample/blob/main/app/src/main/res/values/themes.xml#L55)
- [alert_editor_reset_all](https://github.com/Banuba/ve-sdk-android-integration-sample/blob/main/app/src/main/res/values/themes.xml#L56)
- [alert_editor_reset_effects](https://github.com/Banuba/ve-sdk-android-integration-sample/blob/main/app/src/main/res/values/themes.xml#L57)
