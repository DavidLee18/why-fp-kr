# 소개

이 글은 좀 더 큰 규모의 (함수형이 아닌) 프로그래머 커뮤니티에 함수형 프로그래밍의 중요성을 설명하고, 함수형 프로그래머들이 함수형 프로그래밍의 이점을 완전히 활용할 수 있도록 함수형 프로그래밍의 이점이 무엇인지 명확하게 하려는 시도입니다.

함수형 프로그래밍이 "함수형"이라고 불리는 이유는 그 근본적인 작업이 매개변수들에 함수들을 적용하는 것이기 때문입니다. 메인 프로그램 자체가 프로그램의 입력을 매개변수로 받고 프로그램의 출력을 그 결과로 전달하는 함수로 작성됩니다. 
보통 메인 함수는 다른 함수들을 이용해서 정의되어 있고, 그것들은 또한 더 많은 다른 함수들을 이용해서 정의되는데, 이것은 마지막에 그 함수들이 언어의 기본 작업일 때까지 진행됩니다. 이 모든 함수들은 보통의 수학적 함수들과 매우 비슷하고, 
이 글에서 보통의 등식들로 정의될 것입니다. 우리는 여기서 터너의 언어인 미란다를 사용하지만, 이것에 대한 특별한 지식 없이도 읽을 수 있는 표기법을 사용할 것입니다. 

함수형 프로그래밍의 특별한 특징들과 이점들은 보통 다음과 같이 서술됩니다. 함수형 프로그램은 값의 변경문이 없으므로, 변수는 한번 값을 받으면 절대 변하지 않습니다. 더 일반적으로 말하자면, 함수형 프로그램은 부작용이 전혀 없습니다. 
함수 호출은 그 결과를 계산하는 것 외의 다른 효과를 낼 수 없습니다. 이것은 주요한 버그의 근원을 없애고, 실행 순서를 상관없게 만듭니다 -- 어떤 부작용도 식의 값을 바꿀 수 없으므로, 그 값은 언제 계산되어도 됩니다. 
이것은 프로그래머를 제어 구조를 일일히 지시해야 하는 짐에서 해방시켜 줍니다. 식이 언제 평가되어도 되므로, 변수들을 그 값으로, 또 반대로도 자유롭게 바꿀 수 있습니다 -- 즉, 프로그램은 "참조 투명"합니다. 
이러한 자유는 함수형 프로그램을 전통적인 프로그램보다 수학적으로 다루기 용이하게 해 줍니다. 

이러한 종류의 "이점들"은 매우 좋지만, 외부인들이 이것을 별로 진지하게 보지 않아도 어쩔 수 없습니다. 이것은 함수형 프로그래밍이 무엇이 아닌지에 대해서 많이 이야기하지만 (변경문이 없고, 부작용이 없고, 제어문이 없음) 
함수형 프로그래밍이 무엇인가에 대한 것은 별로 말하지 않습니다. 함수형 프로그래머는 마치 자기가 고결하게 되리라는 희망에 차서, 삶의 즐거움을 절제하는 중세의 수도승같이 느껴집니다. 실리를 더 중시하는 사람들에게 이러한 "이점들"은 전혀 설득력이 없습니다. 

함수형 프로그래머들은 막대한 실질적 이익이 *있다고* 주장합니다 -- 함수형 프로그램은 훨씬 더 길이가 짧기 때문에, 함수형 프로그래머는 전통적인 프로그래머보다 훨씬 더 생산적이라는 거죠. 하지만 이런 일이 일어나는 이유가 뭘까요? 
이러한 "이점들"에 의거하여 그나마 말할 수 있는 이유는 전통적인 프로그램들은 90% 정도가 변경문으로 이루어져 있는데, 함수형 프로그램들에서는 이것들을 생략할 수 있기 때문이라는 겁니다! 이건 그냥 말이 안 됩니다. 
만약 변경문을 생략하는 것이 그러한 엄청난 이익을 가져왔다면 포트란 프로그래머들은 20년 전부터 이것을 실행했을 겁니다. 어떤 언어의 기능을 빼는 것으로 그 언어를 더 강력하게 만든다는 것은 논리적으로 말이 안 됩니다, 그 기능이 아무리 나쁘더라도 말이죠. 

심지어는 함수형 프로그래머조차도 이런 이점이라 불리는 것들에 대해 불만을 가져야 하는데, 이것들이 함수형 프로그래밍의 강력함을 활용하는 데에 아무런 도움을 주지 않기 때문입니다. 변경문이 없거나 참조 투명한 프로그램은 구체적으로 만들 수 없습니다. 여기에는 프로그램의 품질에 대한 기준이 없고, 따라서 지향점도 없는 것이죠. 

확실히 이렇게 함수형 프로그래밍의 특징을 설명하는 것은 부적절합니다. 우리는 이를 대체할 것을 찾아야 합니다 -- 단지 함수형 프로그래밍의 강력함을 설명할 뿐만 아니라 함수형 프로그래머가 나아가야 할 확실한 기준을 제시해 줄 것을 말이죠. 
