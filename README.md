# StarT Translations Manager

A comprehensive translation management system for the Star Technology Minecraft modpack.

## Installation

1. Clone this repository or download the files
2. Ensure you have Python 3.7+ installed
3. Install required dependencies:
   ```bash
   pip install tkinter
   ```
   Note: tkinter usually comes with Python by default

## Usage

### GUI Application

Launch the graphical interface:
```bash
python launch_gui.py
```

#### Main Features:

1. **Open Workspace**: Load your translation files from the `lang` folder
2. **Language Selection**: Choose which language to work on
3. **Category Filtering**: Filter by mod categories and subcategories
4. **Translation Editor**: Edit translations with real-time formatting preview
5. **Formatting Tools**: Add Minecraft color codes and formatting
6. **Search**: Find specific translations quickly
7. **Statistics**: View translation progress

#### Keyboard Shortcuts:
- `Ctrl+O`: Open workspace
- `Ctrl+S`: Save all translations
- `Ctrl+F`: Focus search
- `F5`: Refresh translations

### Command Line Interface

Launch the CLI tool:
```bash
python launch_cli.py <workspace_path> <command>
```

#### Available Commands:

```bash
# List available languages
python launch_cli.py lang list-languages

# List categories
python launch_cli.py lang list-categories

# Add a new language
python launch_cli.py lang add-language fr_fr

# Validate translations
python launch_cli.py lang validate es_es

# Export untranslated keys
python launch_cli.py lang export-untranslated es_es untranslated_es.txt

# Show statistics
python launch_cli.py lang stats es_es
```

## File Structure

```
StarT-Translations/
├── src/                          # Source code
│   ├── translation_manager.py    # Core translation logic
│   ├── translation_gui.py        # GUI application
│   └── translation_cli.py        # CLI tool
├── lang/                         # Translation files
│   ├── core-mod/
│   │   └── en_us.json           # English (base language)
│   ├── gtceu/
│   └── ...
├── launch_gui.py                 # GUI launcher
├── launch_cli.py                 # CLI launcher
└── README.md                     # This file
```

## Adding New Languages

### Using the GUI:
1. Click "Add Language" in the toolbar
2. Enter the language code (e.g., `fr_fr`, `de_de`)
3. All translation keys will be created automatically with empty values

### Using the CLI:
```bash
python launch_cli.py lang add-language fr_fr
```

### Supported Language Codes:
Use standard Minecraft language codes:
- `es_es` - Spanish (Spain)
- `fr_fr` - French (France)
- `de_de` - German (Germany)
- `pt_br` - Portuguese (Brazil)
- `ru_ru` - Russian
- `zh_cn` - Chinese (Simplified)
- `ja_jp` - Japanese
- And many more...

## Minecraft Formatting

The tool supports all Minecraft formatting codes:

### Color Codes:
- `§0` - Black
- `§1` - Dark Blue
- `§2` - Dark Green
- `§3` - Dark Aqua
- `§4` - Dark Red
- `§5` - Dark Purple
- `§6` - Gold
- `§7` - Gray
- `§8` - Dark Gray
- `§9` - Blue
- `§a` - Green
- `§b` - Aqua
- `§c` - Red
- `§d` - Light Purple
- `§e` - Yellow
- `§f` - White

### Formatting Codes:
- `§l` - Bold
- `§o` - Italic
- `§n` - Underline
- `§m` - Strikethrough
- `§k` - Obfuscated
- `§r` - Reset

### Example:
```
§6Gold text §l§cBold Red §rNormal text
```

## Translation Guidelines

### DO:
- ✅ Use proper grammar and spelling in your native language
- ✅ Maintain the same tone and style as the English version
- ✅ Keep formatting codes (`§` codes) in the same positions
- ✅ Preserve placeholders like `%1$s`, `{0}`, etc.
- ✅ Test your translations in-game when possible
- ✅ Keep translations concise while maintaining meaning
- ✅ Use consistent terminology throughout

### DON'T:
- ❌ Use Google Translate or other automatic translation tools
- ❌ Use AI translation tools without human review
- ❌ Remove or modify formatting codes unless necessary
- ❌ Change placeholder order without adjusting the format specifiers
- ❌ Leave translations empty - mark uncertain translations with [TODO] instead
- ❌ Copy-paste English text as translation
- ❌ Use informal language unless the original does

### Special Considerations:
- **Item Names**: Should be concise and descriptive
- **Quest Text**: Can be longer and more descriptive
- **UI Elements**: Should be short to fit interface constraints
- **Technical Terms**: Some mod-specific terms might be better left in English

## Contributing

1. **Fork the repository** or get access to the translation workspace
2. **Choose your language** - check if it already exists
3. **Use the tools** provided to manage translations efficiently
4. **Follow the guidelines** above for quality translations
5. **Test your work** - verify translations work in-game
6. **Submit your changes** through your preferred method (PR, shared folder, etc.)

### Quality Checklist:
- [ ] All translations are human-made, not machine-translated
- [ ] Formatting codes are preserved correctly
- [ ] Placeholders are maintained
- [ ] Grammar and spelling are correct
- [ ] Terminology is consistent
- [ ] Translations fit the context and tone
- [ ] No empty translation entries

## Troubleshooting

### Common Issues:

1. **GUI won't start**:
   - Make sure Python 3.7+ is installed
   - Install tkinter: `pip install tk`
   - Check console for error messages

2. **Can't load workspace**:
   - Verify the `lang` folder exists
   - Check that JSON files are valid
   - Ensure you have read permissions

3. **Translations not saving**:
   - Check write permissions in the `lang` folder
   - Verify JSON file structure
   - Look for error messages in the status bar

4. **Formatting preview not working**:
   - This is normal - the preview is simplified
   - Test formatting codes in-game for best results

### Getting Help:

If you encounter issues:
1. Check the error messages in the application
2. Verify your JSON files are valid
3. Try reloading the workspace
4. Check file permissions
5. Report bugs with detailed error messages

## License

This tool is provided for the Star Technology modpack translation project. Please respect the licensing of the original mod content when contributing translations.

---

Happy translating! 🌟

---

# Korean lang only part

I(peaplant) made resource pack for Star Technology translation!

"Star Technology Korean Translation" resource pack will translating some important things from playthrough.

If you check the mod list, check the inside of "resourcepack file".

If item doesn't used in mod pack, I translated it as "게임에서 사용 안 함"(Not used in game).

## 한국어 설명

Star Technology의 번역을 위해 특별히 만든 리소스팩입니다!

이 리소스팩은 게임을 진행하는데 필요한 중요한 몇몇 모드의 번역이 들어가 있습니다.

이미 번역되어 있는 모드의 경우 따로 번역하지 않았습니다.

"resourcepack files"에서 번역된 모드 ID를 확인 가능합니다

만약 모드팩에서 사용하지 않는 아이템이라면 "게임에서 사용 안 함"또는 "모드팩에서 달성 불가능한 항목입니다"으로  역하였습니다(모드팩에서 사용하는 아이템인데 해당 번역으로 되어 있다면 보고 바랍니다).

### 현재 발견된 문제

#### 제보 방법

해당 문제가 발생하는 상황과 스크린샷, 언어로 영어로 바꿨을 때 나오는 문자열을 공식 디코의 한국어 번역 스레드로 보내주면 됩니다.

