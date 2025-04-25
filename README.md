# vsc_intl_message


Parses and formats [ICU Message strings](http://userguide.icu-project.org/formatparse/messages).

## Usage

    var msg = new IntlMessage("It is now {now, date, long}");
    
    var str = msg.format({
      "now": new DateTime.now()
    });
    
    print(str);
    
    msg = new IntlMessage({
      "nl": "Toon is geboren op {birthday, date, long}",
      "en": "Toon was born on {birthday, date, long}",
    });
    
    IntlMessage.withLocale("nl", () {
      var str = msg.format({
        "birthday": new DateTime(2008,8,16)
      });
    
      print(str);
   
    });
    
    
## Features and bugs

Please file feature requests and bugs at the [issue tracker][tracker].

[tracker]: https://github.com/VisualSystemsCorp/vsc_intl_message/issues

## Sponsor

Forked from https://github.com/appsup-dart/intl_message on 2025-04-25 commit 68f2e5c1214e27d48d1013173989101a6c47daaf.
