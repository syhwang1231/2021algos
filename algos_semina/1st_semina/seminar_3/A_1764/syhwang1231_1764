#include <iostream>
#include <string>
#include <vector>
#include <algorithm>

using namespace std;

int main(void) {
	int notHeard, notSeen;

	string see;

	vector<string> listen;
	vector<string> both;

	cin >> notHeard >> notSeen;

	for (int i = 0; i < notHeard; i++) {  //듣지도 못한 사람들 이름 입력받기
		string notHeardName;
		cin >> notHeardName;
		listen.push_back(notHeardName);
	}

	sort(listen.begin(), listen.end());		//듣지도 못한 사람들을 오름차순으로 정렬

	for (int i = 0; i < notSeen; i++) {   //보지도 못한 사람들 이름 입력받기
		cin >> see;
		if (binary_search(listen.begin(),listen.end(),see))   //이진탐색으로 listen 벡터에 see가 있는지 확인
			both.push_back(see);  //있다면 both에 push
	}

	sort(both.begin(), both.end());   //both를 오름차순으로 정렬(듣지도 보지도 못한 사람들)

	cout << both.size() << "\n";;
	for (int i = 0; i < both.size(); i++)
		cout << both[i] << "\n";

	return 0;
}
