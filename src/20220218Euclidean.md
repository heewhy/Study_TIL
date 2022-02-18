# 유클리드 호제법(Euclidean-algorithm)

- 두 개의 수가 주어졌을 때, 최대 공약수를 구하는 알고리즘

- 두 개의 수 A, B가 존재하고, A를 B로 나눈 나머지를 C라면,  

<pre>
<code>
/**
	 * 최대 공약수를 찾는 함수
	 * @param a 최대공약수를 찾는 첫번째 숫자
	 * @param b 최대공약수를 찾는 두번째 숫자
	 * @return 최대공약수
	 */
private static int gcd(int a, int b) {
		//기저조건
		if (b == 0)
			return a;
            
		// GCD(a, b) = GCD(b, r)이므로 (r = a % b)
		return gcd(b, a % b);
	}
</code>
</pre>

