localizationStateSelector
^^^^^^^^^^^^^^^^^^^^^^^^^

:aspect:`Datatype`
    array

:aspect:`Scope`
    fieldWizard

:aspect:`Description`
    The localization state selector wizard displays two or three radio buttons in localized records
    saying: "This field has an own value distinct from my default language or source record", "This field
    has the same value as the default language record" or "This field has the same value as my source record".
    This wizard is especially useful for the :php:`tt_content` table. It will only render, if:

    * The record is a localized record (not default language)
    * The record is in "translated" (connected), but not in "copy" (free) mode
    * The table is localization aware using the ['ctrl'] properties :ref:`languageField <ctrl-reference-languagefield>`,
      :ref:`transOrigPointerField <ctrl-reference-transorigpointerfield>`. If the optional property
      :ref:`translationSource <ctrl-reference-translationSource>` is also set, and if the record is a translation
      from another localized record, the third radio appears.
    * The property ['config']['behaviour']['allowLanguageSynchronization'] is set to true

    .. figure:: ../../Images/FieldWizardLocalizationStateSelector.png
        :alt: Example localization state selector on a type=input field
        :class: with-shadow

        Example localization state selector on an type=input field