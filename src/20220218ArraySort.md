# compare(),compareTo()

- compare(), compareTo()

    - compare() : Comparator 인터페이스를 구현할 때 작성해야하는 메서드
    - 실제로 구현할 떄 compare()에 2개의 인자를 넘겨 내부에 구현에 따라 int 결과 값을 리턴
    <pre>
    <code>
        @Override
        public int compare(o1,o2){
            if(o1>o2){
                return 1;
            }else if(o1<o2){
                return -1;
            }else{
                return 0;
            }
        }

        //람다
        Arrays.sort(point,(a,b)->{
			if(a[0]==b[0]) return a[1]-b[1];
			else return a[0]-b[0];
		});
        //2
        Arrays.sort(N, (a,b)->a.age-b.age);

    </code>
    </pre>

    -  compareTo()
    - 문자열, primitive data type 의 비교

    <pre>
    <code>
        str.compareTo(str2);
        Integer.compareTo(o2);
    </code>
    </pre>

- compare() 메서드는 Comparator 인터페이스를 구현할 때 구현해야하는 메서드
- 메소드에 두 개의 객체를 전달 가능 관계를 설명하는 int 반환

