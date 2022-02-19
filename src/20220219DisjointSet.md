# 서로소 집합, 합집합-찾기 자료구조 

- union-find 자료 구조라고도 불림

- find : 어떤 원소가 주어졌을 때 이 원소가 속한 집합을 반환, 부모확인

- union : 두 개의 집합을 하나로 합친다. , 사이클인지 확인

<pre>
<code>
    public static int find(int a) {
		//정점이 처음 등장 하면 자기 자신이 부모
		if(a==parent[a]) return a;
		//find 할때 마다 부모는 최상위 부모로 설정
		parent[a] = find(parent[a]);
		return parent[a];
	}
	
	public static void union(int a,int b) {
		int aRoot = find(a);
		int bRoot = find(b);
		
		if(aRoot!=bRoot) {
			parent[aRoot]=b;
		}else {
			return;
		}
	}

</code>
</pre>



