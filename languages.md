# Languages

## Language settings[¶](languages.md#language-settings) <a id="language-settings"></a>

Summary

In this quick tutorial we will learn how to install, activate, and manage language packages for Panda.

### Show active language[¶](languages.md#show-active-language) <a id="show-active-language"></a>

Command

Get the current default language.

```text
wp language core list --status=active
```

Example

The output might look as follows.

| **Language** | **English name** | **Native name** | **Status** | **Update** |
| :--- | :--- | :--- | :--- | :--- |
| en\_US | English \(United States\) | English \(United States\) | active | none |

### Install new languages[¶](languages.md#install-new-languages) <a id="install-new-languages"></a>

Command

Install the German core language packages.

```text
wp language core install de_AT de_CH de_CH_informal de_DE de_DE_formal
```

Output

Success: Installed 5 of 5 languages.

### List installed languages[¶](languages.md#list-installed-languages) <a id="list-installed-languages"></a>

Command

List installed core language packages.

```text
wp language core list --status=installed
```

Example

The output might look as follows.

| **Language** | **English name** | **Native name** | **Status** | **Updated** |
| :--- | :--- | :--- | :--- | :--- |
| de\_AT | German \(Austria\) | Deutsch \(Österreich\) | installed | 2020-09-13 17:09:13 |
| de\_CH | German \(Switzerland\) | Deutsch \(Schweiz\) | installed | 2020-09-09 20:03:38 |
| de\_CH\_informal | German \(Switzerland, Informal\) | Deutsch \(Schweiz, Du\) | installed | 2020-09-09 20:03:47 |
| de\_DE | German | Deutsch | installed | 2020-10-22 11:22:21 |
| de\_DE\_formal | German \(Formal\) | Deutsch \(Sie\) | installed | 2020-10-22 11:23:04 |

### Switch default language[¶](languages.md#switch-default-language) <a id="switch-default-language"></a>

Command

Set German as default language.

```text
wp site switch-language de_DE
```

Output

Success: Language activated.

### Install theme language[¶](languages.md#install-theme-language) <a id="install-theme-language"></a>

Command

Install the German language packages for the Twenty Twenty theme.

```text
wp language theme install twentytwenty de_CH de_CH_informal de_DE de_DE_formal
```

Output

Success: Installed 4 of 4 languages.

### Install plugin language[¶](languages.md#install-plugin-language) <a id="install-plugin-language"></a>

Command

Install the German language packages for WooCommerce.

```text
wp language plugin install woocommerce de_CH de_CH_informal de_DE de_DE_formal
```

Output

Success: Installed 4 of 4 languages.

### Update language packages[¶](languages.md#update-language-packages) <a id="update-language-packages"></a>

Command

Update all core language packages if needed.

Output

Success: Translations are up to date.

Command

Update all plugin language packages if needed.

```text
wp language plugin --all update
```

Output

Success: Translations are up to date.

Command

Update all theme language packages if needed.

```text
wp language theme --all update
```

Output

Success: Translations are up to date.

### Getting help[¶](languages.md#getting-help) <a id="getting-help"></a>

[Click here to see the full documentation… ]()

 Last update: January 24, 2021

