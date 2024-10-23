# Develop with Apps Script and AppSheet: Challenge Lab || ARC126 ||

### **Solution Video:** [Watch Here]()

### Task 1.

1. ATM Maintenance Tracker

2. link Driver [here](https://drive.google.com/drive/my-drive)

3. link File [here](https://stdntpartners-my.sharepoint.com/:f:/g/personal/gaston_condori_studentambassadors_com/ErsD25JRd0hCtkb9gjJ9FYkBMBGsf8UVjR9vyP97OqHNZw?e=MD5x6J)

4. link Apps Script Chat App [here](https://script.google.com/home/projects/create?template=hangoutsChat)

```
/**
 * Responds to a MESSAGE event in Google Chat.
 *
 * @param {Object} event the event object from Google Chat
 */
function onMessage(event) {
  var name = "";

  if (event.space.type == "DM") {
    name = "You";
  } else {
    name = event.user.displayName;
  }
  var message = name + " said \"" + event.message.text + "\"";

  return { "text": message };
}

/**
 * Responds to an ADDED_TO_SPACE event in Google Chat.
 *
 * @param {Object} event the event object from Google Chat
 */
function onAddToSpace(event) {
  var message = "";

  if (event.space.singleUserBotDm) {
    message = "Thank you for adding me to a DM, " + event.user.displayName + "!";
  } else {
    message = "Thank you for adding me to " +
        (event.space.displayName ? event.space.displayName : "this chat");
  }

  if (event.message) {
    // Bot added through @mention.
    message = message + " and you said: \"" + event.message.text + "\"";
  }
  console.log('Helper Bot added in ', event.space.name);
  return { "text": message };
}

/**
 * Responds to a REMOVED_FROM_SPACE event in Google Chat.
 *
 * @param {Object} event the event object from Google Chat
 */
function onRemoveFromSpace(event) {
  console.info("Bot removed from ",
      (event.space.name ? event.space.name : "this chat"));
}

```

5. Link **OAuth consent screen** [here](https://console.cloud.google.com/apis/credentials/consent?)

6. App name : | Helper Bot |

7. Link **Google Chat API Configuration** [here](https://console.cloud.google.com/apis/api/chat.googleapis.com/hangouts-chat?)

8. App name : | Helper Bot |

9. Avatar URL : | https://goo.gl/kv2ENA |

10. Description | Helper chat bot |

11. Link **Helper Bot** [here](https://mail.google.com/chat/u/0/#chat/home)

### Kudos 🌟 on completing the lab!

#### You’ve brilliantly showcased your talent and dedication.

### Keep it up!

### don't forget to follow [here](https://youtube.com/@hellodev1?si=1GE3_P0V8xbViLhc)
