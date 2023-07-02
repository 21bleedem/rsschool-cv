# Arman Akopyan

## Contacts
* **Discord** @21bleedem
* **Genius:** [21bleedem](https://genius.com/21bleedem)
* **GitHub:** [21bleedem](https://github.com/21bleedem)
* **Instagram:** [21bleedem](https://instagram.com/21bleedem)
* **SoundCloud:** [21bleedem](https://soundcloud.com/21bleedem)
* **Twitter:** [21bleedem](https://twitter.com/21bleedem)
* **YouTube:** [21bleedem](https://youtube.com/c/21bleedem?sub_confirmation=1)

## Summary
I'm studying at BSUIR. I enjoy creating websites, desktop & web applications. I read articles and listen to podcasts about front-end (Web Standards, Medium) / back-end (Habr). I aspire to develop my skills in learning new technologies & sharing my knowledge with others.

In addition, I professionally transcribe and format music lyrics and write annotations according to the strict standards of the Genius site. The main genres I work with are West Coast and Cali Rap.

## Skills
**🌝 Frontend:**
* TypeScript
* NextJS / ReactJS
* SCSS / styled-components / PostCSS
* Twitter Bootstrap / Ant Design / Tailwind CSS
* Webpack / Gulp
* ESLint / Prettier

**🌚 Backend:**
* Node.JS / C# / Java
* Thymeleaf
* Spring Boot / ASP.NET / Express
* TypeORM / Hibernate
* Oracle / MySQL / Microsoft SQL Server / PostgreSQL / MongoDB
* JWT / Session / PassportJS

**✍️  Other:**
* Git / GitHub
* Adobe Photoshop / Figma
* VS Code, IntelliJ IDEA, Visual Studio

## Code Example
```c#
public static void Load(DataGridView dataGridView, string dbString, string query, int columnsMode) {
  try {
    using(cc.con = new SQLiteConnection(dbString)) {
      cc.con.Open();
      using(cc.cmd = new SQLiteCommand(query, cc.con)) {
        using(cc.rdr = cc.cmd.ExecuteReader()) {
          dataGridView.Rows.Clear();
          dataGridView.AutoSizeColumnsMode = DataGridViewAutoSizeColumnsMode.None;
          while (cc.rdr.Read()) {
            object[] array = new object[] {};
            for (int i = 0; i < dataGridView.Columns.Count; i++) {
              array = array.Concat(new object[] {
                cc.rdr[i]
              }).ToArray();
            }
            dataGridView.Rows.Add(string.Join(",", array).Split(','));
          }
          dataGridView.ClearSelection();
          switch (columnsMode) {
          case 0:
            dataGridView.AutoSizeColumnsMode = DataGridViewAutoSizeColumnsMode.AllCells;
            break;
          case 1:
            dataGridView.AutoSizeColumnsMode = DataGridViewAutoSizeColumnsMode.ColumnHeader;
            break;
          case 2:
            dataGridView.AutoSizeColumnsMode = DataGridViewAutoSizeColumnsMode.DisplayedCells;
            break;
          case 3:
            dataGridView.AutoSizeColumnsMode = DataGridViewAutoSizeColumnsMode.Fill;
            break;
          case 4:
            dataGridView.AutoSizeColumnsMode = DataGridViewAutoSizeColumnsMode.None;
            break;
          }
        }
      }
    }
  }
  catch(Exception ex) {
    MessageBox.Show(ex.Message, "Ошибка", MessageBoxButtons.OK, MessageBoxIcon.Error);
  }
}
```

## Education
* **Belarusian State University of Informatics and Radioelectronics**
  * Faculty of Computer Technologies

## Languages
* **Russian** - native
* **English** - B1
