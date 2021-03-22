cout은 default notation 으로 meaningful digit까지만 표기하고 소수점 뒷자리를 0으로 채우지 않는다   
		따라서 meaningful digit의 범위를 넘는 4.0혹은 4.000000의 경우 원하는 소수점을 정확히 표기하기 위해 fixed notation을 설정해주어야 한다.   
		방법    
		{   
			표기하고자 하는 소수점 출력 이전에 std::cout.precision(number);를 설정해준다   
			이 때, number만큼의 자리수까지만 출력하고 그 아래는 반올림 된다.   
		}   
		참고사항    
		{   
			cout << fixed; 또는 << showpoint를 입력해주지 않고 cout.precision(number)만 입력한 경우   
			integer형태로만 출력된다   
			cout.precision(number)는 소수점 몇째 자리의 숫자까지 출력할 것인가를 정해줄 뿐   
			fixed notation을 강제하지 않는다.   
			따라서 fixed notation을 강제하기 위해선   
			cout << fixed;   
			또는   
			<< showpoint를 입력해서 고정 소숫점 표기 방식을 강제 해줘야 한다.   
		}   
