�Ŵ󾵣����ڸ��û��ṩһ���鿴��Ʒ��ϸ��Ϣ�ķ�ʽ

���桢Ч�������һ��Сͼ����������ƶ����Ҳ���ʾ��Ӧλ�õĴ�ͼ

ʵ��Ҫ�㣺
1������С����move���ƶ��¼�,Ϊ�˲����������move���Ͱ��ƶ��¼�������   move�ĸ���Ԫ��small��
   var newLeft = e.pageX - move.offsetWidth / 2 - show.offestLeft;
   var newTop = e.pageY - move.offsetHeight / 2 - show.offsetTop;

ע�⣺���Ĳο��㣺һ��Ҫ���ĵ������Ͻǣ������ǿ���������Ļ�����Ͻ�


2�������ٽ����ж�
   ˮƽ������ٽ�㣺
	if(newLeft <= 0){ newLeft = 0 ;}
	if(newLeft >= (small.offsetWidth - move.offsetWidth)){
	    newLeft = (small.offsetWidth - move.offsetWidth;
	}
   ��ֱ������ٽ�㣺
	if(newTop <= 0){ newTop = 0 ;}
	if(newTop >= (small.offsetHeight - move.offsetHeight)){
	    newTop = (small.offsetHeight - move.offsetHeight;
	}

3����С�����ƶ�ʱ���ұߵĴ�ͼ��ν����ƶ���ʾ��
   ���ݵȱ�����ʾԭ��
	С����.newLeft / small.width = bigPic.newLeft / bigPic.width
        С����.newTop / small.Height = bigPic.newTop / bigPic.height


     newLeft / small.offsetWidth = newBigPicLeft / bigPic.offsetWidth
     newTop / small.offsetHeight = newBigPicTop / bigPic.offsetHeight

==>>var newBigPicLeft  
==>>var newBigPicTop

ע�⣺�������ƶ�����ͼ���������ƶ���ע������top��left�Ǹ�ֵ��

4������Ŀ�� / small�Ŀ�� = big�Ŀ�� / ͼƬ����Ŀ��
==>>���Եó�����ľ�����

5����ʼ״̬ʱ��big��move����ʾ

6������small��������롢�뿪�¼�

7��������Ʒ�б�,�ٶ�����Ʒ�б�������������¼�
   �����������Ʒ�б���Сͼ��������ʾ��Ӧ��ͼƬ