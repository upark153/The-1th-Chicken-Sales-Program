# The-1th-Chicken-Sales-Program
Chicken sales were programmed with the Python console.
![image](https://user-images.githubusercontent.com/115389450/233535820-e9514b25-a2ed-4cb9-bca9-34efe47a6610.png)
![image](https://user-images.githubusercontent.com/115389450/233535850-8ddcf230-90d6-46bd-8016-7284da7d9e9e.png)
![image](https://user-images.githubusercontent.com/115389450/233535877-c77f7090-c79d-4a20-bf89-767160ef978b.png)
![image](https://user-images.githubusercontent.com/115389450/233535896-0479d9dd-b771-4d10-9c37-0956fe0a8056.png)
![image](https://user-images.githubusercontent.com/115389450/233535927-d9e8f514-f554-4efa-9747-ec41fc5e0d5f.png)
![image](https://user-images.githubusercontent.com/115389450/233535951-6d18bc63-bd06-4fd4-893f-8f5fa6e99efc.png)
![image](https://user-images.githubusercontent.com/115389450/233535973-672f39cc-d7ac-422d-a391-e9953437fa2a.png)
```
def refund(guest):
    claim = guest * 0.15
    print(f'방문한 손님 중 15%가 불만을 풀고 있습니다. 불만을 품은 사람은 {round(claim)}명입니다.')
    cnt = 0
    for k in range(round(claim)):
        a = random.randint(0, 2)
        if a==0:
            # print("클레임을 걸었습니다.!")
            cnt += 1
        else:
            continue
            # print("클레임을 안걸고 무사히 넘어갔습니다 !")

    print(f'클레임을 건 사람은 총 {cnt}명입니다.')

    return cnt
```
```
def refund(guest, daily_sum):
    claim = guest * 0.15
    print(f'방문한 손님 중 15%가 불만을 풀고 있습니다. 불만을 품은 사람은 {round(claim)}명입니다.')
    cnt = 0
    for k in range(round(claim)):
        a = random.randint(0, 2)
        if a==0:
            cnt += 1
        else:
            continue

    print(f'클레임을 건 사람(환불 요청한 사람)은 총 {cnt}명입니다.')
    receive = int((daily_sum * (cnt*0.01)) * 2)
    print(f'환불 해줘야 할 금액은 {receive}원입니다.')
    finalDaily_sum = daily_sum - receive
    print(f'수고하셨습니다. 최종 매출은 {finalDaily_sum}원입니다.')
    return finalDaily_sum
```
![image](https://user-images.githubusercontent.com/115389450/233536101-8b6644f0-6862-4d90-af0e-b39273dcd065.png)
![image](https://user-images.githubusercontent.com/115389450/233536214-883fb62c-d4aa-4191-8449-296156c9356a.png)
![image](https://user-images.githubusercontent.com/115389450/233536252-5553b00d-d46d-45cd-8385-b8adbdd35589.png)
![image](https://user-images.githubusercontent.com/115389450/233536294-2d9ea38f-a0cb-409c-9db2-bacbea95b1b8.png)
```
def refund(rf_guest, rf_daily_sum):
    # 리펀드 함수의 지역변수 claim에 인자값으로 받은 손님 수 * 0.15 해줬음
    claim = rf_guest * 0.15
    # round함수로 클레임이 소수가 나오면 반올림 시킴
    print(f'{rf_guest}명의 손님 중 15%가 불만을 풀고 있습니다. 불만을 품은 사람은 {round(claim)}명입니다.')

    # 클레임을 진짜 걸어버린 손님을 세는 변수 (불만이 있어도 그냥 가거나 클레임을 거는 손님들이 있으니까)
    claim_cnt = 0
    # 전체 손님의 15%(소수면 반올림) 수만큼 반복
    for k in range(round(claim)):
        # 방문한 손님의 15%가 불만을 품어도 클레임을 걸 확률은 50대50
        a = random.randrange(2)
        # a가 0이 나오면 클레임을 검
        if a == 0:
            claim_cnt += 1
        # a가 0이 아닌 그 외의 값이 나오면 클레임을 걸지 않음
        else:
            continue
    # print(f'클레임을 건 사람(환불 요청한 사람)은 총 {claim_cnt}명입니다.')

    # refund함수의 환불 변수(receive) = 하루 매출 * (클레임 건 사람 * 0.01) * 2
    # receive = int((rf_daily_sum * (claim_cnt * 0.01)) * 2)

    # refund함수의 환불 변수(rf_refund) = 하루 매출 * (클레임 건 사람 / 총 손님 수) * 2
    rf_refund = int((rf_daily_sum * (claim_cnt / rf_guest)) * 2)
    print(f'환불 해줘야 할 금액은 {rf_refund}원입니다.')

    # addClaim_daily_sum 변수 = (하루매출) - (환불금액)
    addClaim_daily_sum = rf_daily_sum - rf_refund
    print(f'수고하셨습니다. 최종 매출은 {addClaim_daily_sum}원입니다.')
    return addClaim_daily_sum
```
![image](https://user-images.githubusercontent.com/115389450/233536352-cdcf45a4-3348-47ce-bdc2-63f9f0aac1cc.png)
![image](https://user-images.githubusercontent.com/115389450/233536378-f722f355-04d1-4b5b-804b-770d9a125188.png)
![image](https://user-images.githubusercontent.com/115389450/233536402-3910441d-1606-4a2d-ad65-6104c4ea9d32.png)
![image](https://user-images.githubusercontent.com/115389450/233536423-40a70e44-c3d8-4a8e-91c5-a7520849b35c.png)
![image](https://user-images.githubusercontent.com/115389450/233536508-b2b90ca3-dccc-4097-b8f8-0cd1011af4d3.png)
![image](https://user-images.githubusercontent.com/115389450/233536535-1e53335c-5315-46f2-90ac-2f9857ec6d81.png)
```
 def poison(claim_cnt):
        foodPoisoning = [['CT촬영', 300000], ['X-ray', 100000], ['대변검사', 50000], ['피검사', 50000],
                         ['심전도검사', 50000], ['내과초음파', 50000], ['산부인과초음파', 50000],
                         ['영양제', 300000], ['직장내시경', 100000]]

        hospitalBill = 0  # 병원비# 는 처음에 0원

        patient = claim_cnt * 0.1  # 클레임 건 사람을 매개변수로 받아서 그 중의 10%가 환자

        print(f'{claim_cnt}명중 10%인 {round(patient)}명이 병원에 가겠다고 난동을 피우고 있습니다.')

        patient_cnt = 0  # 병원에 가는 진짜 손님을 세는 변수 (병원을 갈 수도, 자가치료 할수도 있음(착하면))
        for i in range(round(patient)):
            a = random.randrange(2)  # 식중독에 걸릴수도, 안걸리수도 있는 50대 50의 확률로 다시 반복한다.
            # a가 0이 나오면 병원에 입원 함.
            if a == 0:
                patient_cnt += 1
            else:
                continue
        print(f'병원을 가겠다고 병원비를 요구한 사람은 총 {patient_cnt}명 입니다.')

        for h in range(patient_cnt):  # 병원을 가겠다고 한 사람만큼 반복문 돌림
            # 병원비에 들어갈 항목 선택
            num_foodPoisoning = random.randint(1, 10) # 병원 진료 항목이 총 9개이므로, 랜덤으로 진료받을 항목 선택
            # 병원에 가겠다고 한 사람이 병원 진료 받은 내역(영수증)
            ds_patient_sum = 0 

            # 병원 진료 받은 내역(랜덤으로 고른 병원 진료 수) 만큼 반복문 돌림.
            for num in range(num_foodPoisoning):
                # 0번 진료부터 8번 진료까지 8가지 진료 인덱스 번호를 하나 고르게 합니다.
                choose_foodPoisoning = random.randrange(9)
                # j에 0부터 8까지 숫자 들어감
                for j in range(9):
                    if choose_foodPoisoning == j:  # 손님이 고른 병원진료 항목 인데스번호와 j가 같으면 실행
                        ds_patient_sum += foodPoisoning[j][1] # 진료항목 금액을 합산함.

            hospitalBill += ds_patient_sum # 병원비에 합산함(진료 항목)

        # print(f'병원비는 총 {hospitalBill}이 나왔습니다. ')

        return hospitalBill # 병원비 값을 리턴하여 값 저장.
```
![image](https://user-images.githubusercontent.com/115389450/233536602-0c8662d9-3a2c-4ca6-8ea7-01308363dad9.png)
![image](https://user-images.githubusercontent.com/115389450/233536621-59f48256-6697-4cf7-a6b7-74ab6a9dc2ce.png)
![image](https://user-images.githubusercontent.com/115389450/233536686-d3a08beb-2c56-4760-8b8c-ef731c6f2513.png)
![image](https://user-images.githubusercontent.com/115389450/233536727-38d5b3f7-056a-4e4c-9e33-39c0f5ffd202.png)
![image](https://user-images.githubusercontent.com/115389450/233536771-f73d6d28-e6f6-4097-95ff-e5454abc1810.png)
![image](https://user-images.githubusercontent.com/115389450/233536809-d4586255-9648-4e37-8d22-ca9f30dc4191.png)
```
import random
# 위생점검은 하루하루 매일 옴 한달동안 무조건
# 손님, 하루 매출을 받아서 일 매출에 영향을 주는 함수
maintainance = {'개인위생관리': 0, '식재료검수': 0, '조리관리': 0, '시설관리': 0}

# print(maintainance['개인위생관리'])
# print(maintainance['식재료검수'])
# print(maintainance['조리관리'])
# print(maintainance['시설관리'])
for key in maintainance:
    a = random.randint(1, 10)
    # maintainance.update(value=a)
    maintainance[key] = a
print(maintainance)
```
![image](https://user-images.githubusercontent.com/115389450/233536853-0c0aaa97-2c13-4e4f-acb0-b0c0bc226899.png)
![image](https://user-images.githubusercontent.com/115389450/233536888-6356b2f5-928f-4df2-ab2d-4ce8f3dcfa9a.png)
```
    def hygiene(gn_guest):
        print("\n보건소 위생점검 공무원이 방문했습니다. 위생점검을 시작합니다.\n")
        maintainance = {'개인위생관리': 0, '식재료검수': 0, '조리관리': 0, '시설관리': 0} #딕셔너리를 이용하여, 위생점수 0점에서 시작

        for key in maintainance: # 딕셔너리 key값 만큼 반복한다.
            a = random.randint(1, 10) # 각 항목별로 점수는 1점에서 10점 랜덤으로 매겨짐
            maintainance[key] = a # 랜덤으로 나온 값을 value값에 넣어줌
        print(maintainance) # 위생점검 끝난 후 value 값 표시
        hygieneScore = sum(maintainance.values()) #위생점수의 합을 새로운 변수에 넣어줌
        print(f"위생점수는 {hygieneScore}점 입니다.")
        if hygieneScore >= 20: # 20점의기준은? 만점이 40점이라 공정하게 절반 생각했습니다.
            print("위생점검 합격입니다. 손님이 20% 증가합니다.")
            hy_gn_guest = round(gn_guest * 1.2) # round는 반올림함수 소수점 값 제거를 위해 사용함.
            return hy_gn_guest
        elif hygieneScore < 20:
            print("위생점검 불합격입니다.손님이 20% 감소합니다.")
            hy_gn_guest = round(gn_guest * 0.8)
            return hy_gn_guest
        elif hygieneScore == 40: # 10점이 4번 나오는 경우 완벽한 위생상태 잭팟
            print("국가에서 인증받은 기관입니다. 손님이 50% 증가합니다.")
            hy_gn_guest = round(gn_guest * 1.5)
            return hy_gn_guest
        elif hygieneScore == 4: # 1점이 4번 나오는 경우 최악의 위생상태 똥망
            print("국가에 위생점검 표적 대상이 되었습니다. 손님이 50% 감소합니다. ")
            hy_gn_guest = round(gn_guest * 0.5)
            return hy_gn_guest

    hygiene_guest = hygiene(gn_guest) #함수리턴 값을 받아서 새로운 변수에 저장
```
![image](https://user-images.githubusercontent.com/115389450/233536941-4ee8d60d-d81a-49a7-9078-54fede8d07dd.png)
[딕셔너리 참조사이트](https://hun931018.tistory.com/56)
[딕셔너리 밸류값 참조](https://www.delftstack.com/ko/howto/python/python-sum-dictionary-values/)

![image](https://user-images.githubusercontent.com/115389450/233544051-4a2e1fab-32f7-428b-abb6-1ffc929ed65f.png)
![image](https://user-images.githubusercontent.com/115389450/233544078-3443582d-f330-43a6-b6f7-6a5834544d4f.png)
![image](https://user-images.githubusercontent.com/115389450/233544115-1ee40111-cde2-44f5-81f3-1eecd304b586.png)
![image](https://user-images.githubusercontent.com/115389450/233544144-90cdebf3-21c9-4a3f-b2c8-155aa7e69582.png)
![image](https://user-images.githubusercontent.com/115389450/233544173-bb5ab93e-e19e-4a8d-ae80-e84b9b379e22.png)
[구조도 참고한 사이트](http://www.tcpschool.com/codingmath/flowchart)





