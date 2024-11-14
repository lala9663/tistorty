# TiStory ✍🏼

## 블로그 꾸준히 작성하기

## 📕 Latest Blog Posts

<ul><li><a href="https://lala9663.tistory.com/169">LLM 과 임베딩</a></li><li><a href="https://lala9663.tistory.com/168">RPA가 뭐지?</a></li><li><a href="https://lala9663.tistory.com/167">DDOS(디도스) 이건 어떤 공격이지?</a></li><li><a href="https://lala9663.tistory.com/166">[Spring] java.lang.IllegalArgumentException: Name for argument of type [java.lang.Long] not specified, and parameter name information not available via reflection.</a></li><li><a href="https://lala9663.tistory.com/165">이벤트: 캡처링과 버블링의 원리와 활용</a></li></ul>



var parseData = JSON.parse(sortingInput);

function createAdaptiveCard(parseData) {
    var adaptiveCard = {
        "$schema": "http://adaptivecards.io/schemas/adaptive-card.json",
        "type": "AdaptiveCard",
        "version": "1.3",
        "body": [],
        "actions": []
    };
adaptiveCard.body.push({
    "type": "TextBlock",
    "text": "실행할 과제: " + totalProcess,
    "size": "Large",  
    "weight": "Bolder",  
    "spacing": "None",   // 상단에 붙이기 위해 간격을 제거
    "wrap": true  // 텍스트가 길 경우 자동으로 줄바꿈
});

        for (var i = 0; i < parseData.length; i++) {
        var name = parseData[i];
        adaptiveCard.body.push({
            "type": "TextBlock",
            "text": name + " 값을 입력해주세요",
            "wrap": true
        });

        adaptiveCard.body.push({
            "type": "Input.Text",
            "id": name,
            "placeholder": name + " 값을 입력"
        });
    }
    
    adaptiveCard.actions.push({
        "type": "Action.Submit",
        "title": "Submit"
    });
    
    return adaptiveCard;
 }

// Adaptive Card JSON 생성
var card = createAdaptiveCard(parseData);
