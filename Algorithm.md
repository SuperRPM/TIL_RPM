 - Shortest Path
 최단경로 알고리즘
 
그래프로 최단경로르 찾아내는 알고리즘을 만들어 내는데
그래프 안에서는

1. 방향성
2. 가중치
3. 음수 엣지
4. 무방향
5. 싸이클


등 여러가지 요소들이 있어서 최단경로를 구하는 알고리즘도 마찬가지로 여러개이다

 * BFS


 각 노드의 앞순서의 노드 정보를 저장한 pre_node를 통해서 연결된 이전 노드의 정보를 저장해준다.
 주의! 인접한 노드의 정보를 저장하는것과는 다르다.
 다만 알고리즘에서는 일반적으로predecessor라고 하는것 같다.
 
 **backtracking**
 
 A - B - D
 
 의 경로를 구한다고 할때
 목적지 D의 노드를 기준으로 predecessor를 추적하여 A까지 도착하는것을 백트랙킹이라고 한다.
 
 '''python
 def back_track(destination_node):
    """최단 경로를 찾기 위한 back tracking 함수"""
    res_str = ""  # 리턴할 결과 문자열
    new_str = ""
    # 코드를 쓰세요
    current_node = destination_node
    while current_node.predecessor != None:
        #print(current_node.station_name, current_node.predecessor.station_name)
        res_str = current_node.predecessor.station_name + ' ' + res_str
        current_node = current_node.predecessor
    res_str += destination_node.station_name
    return res_str
 '''
how to backtracking
