# Песочница Miko

Вы можете использовать это публично, как обычную песочницу. Только пожалуйста, ***НИКОГДА не*** коммитьте её.

<!-- tabs:start -->

### **python**

импортируйте это

```py
import base64

def decode_level_password(password: str) -> str:
    # decode the password from base64
    decoded_base64 = base64.b64decode(password.encode()).decode()
    # put it through the xor cipher with the key "26364")
    decoded = xor_cipher(decoded_base64, "26364")

    return decoded
```

### **java**

пошло оно нахуй

<!-- tabs:end -->

\* = тебе нравятся дисклеймеры? мне вот нет

<div class="projects_card">
    <a href="$" class="project_card_background-container">         
        <img class="project_card-background" src="https://pbs.twimg.com/media/ESu_msLVAAAT_qn?format=jpg&name=large" alt="background">
        <div class="project_card-background-overlay"></div>
    </a>
    <div class="projects_card-card">
        <div class="projects_card_content projects_card_content-details">
            <div class="projects_card_logo">
                <img class="projects_card_logo-image" src="https://raw.githubusercontent.com/gd-programming/gddocs/master/assets/gddocs-icon.png">
            </div>
            <div class="projects_card_details">
                <div class="projects_card_title">
                    <div class="u-ellipsis-overflow">
                       GDDocs
                    </div>
                </div>
                <div class="projects_card_authors">
                <div class="u-ellipsis-overflow">
                        Команда GDProgramming
                    </div>
                </div>
            </div>
        </div>
        <div class="projects_card_content projects_card_content-stats">
            <div class="projects_card_stats">
                <div class="projects_card_language-icon-container">
                    <div class="projects_card_language-icon projects_card_language-icon--html"></div>
                </div>
                <div class="projects_card_language-message u-ellipsis-overflow">HTML</div>
            </div>
        </div>
    </div>
</div>