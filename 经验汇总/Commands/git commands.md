### Git�����������

#### ��һ��ʹ��

	- ��ʼ����
	$git config --global user.name 'name'
	$git config --global user.email 'xxx@xx.com'

	- ��ʼ��
	$git init

	- ����GitHub��gitee
	$ssh-keygen -t rsa -C 'xxx@xx.com'
	$cd ~/.ssh
	$ls
	$cat id_rsa.pub
	������Կ��ӵ�GitHub��gitee�ϵ�settings���ssh��
	$git remote add github git@github.com:xcalan/learn_git.git
	$git remote add gitee git@gitee.com:xcalan/learn_git.git

	- ��һ�ν������ؿ��github����ϵ
	$git pull github master

	- �ύ���ݴ����ͱ��زֿ�
	$git add filename
	$git commit -m 'description'

	- ��һ��push��github
	$git push github master

	- ��һ�ν������ؿ��gitee����ϵ
	$git pull gitee master
	�������conflict���޸ĳ�ͻ���ֶ��ϲ�֮��
	$git add '�޸ĺõ��ļ���'
	$git commit -m 'description'

	- ��һ��push��gitee
	$git push gitee master

#### ���ؿ��github��gitee������֮��ĸ��ºϲ�
	
	- ֻ�б��ظ���
	$git add filename
	$git commit -m 'description'
	$git push github master
	$git push gitee master

	- ���ؿ��Զ�̿ⶼ�и��µ�����µĺϲ�����github�и���Ϊ��
	$git fetch github master
	$git merge github/master
	��ʾ��ͻ���ֶ��޸ĺϲ�Ҫ���������ݺ�
	$git add filename
	$git commit -m 'description'
	$git push github master

	- ���ؿ⡢github��gitee�����ط�ͬʱ�����޸ĺ�ĺϲ����Ƚ�������֮��ĸ��½��кϲ��������������кϲ���
	$git fetch github master
	$git merge github/master
	�������conflict���ֶ��޸ĺϲ�����֮��
	$git add filename
	$git commit -m 'description'
	$git push github master
	$git fetch gitee master
	$git merge gittee/master
	�������conflict���ֶ��޸ĺϲ�����֮��
	$git add filename
	$git commit -m 'description'
	$git push gitee master
	(���������ĺϲ���


#### �������
	
	$git branch ��֧����	//������֧

	
	$git checkout ��֧����	//�л���֧
	$git switch ��֧����

	$git branch	//�鿴��֧������Ҫ������Զ�̿����ϵ�Ժ�ſ��Բ鿴��
			
	$git remote -v	//�鿴������Զ�̿����Ϣ

	$git status	//�鿴��ǰ���״̬
	$git diff	//�鿴��ǰ�����һ���ύ�޸ĵ�����

	$git merge ��֧����	//ָ����֧�ϲ�����ǰ��֧��
	$git branch -d ��֧���� //ɾ����֧

	$git log --graph	//�鿴��֧�ϲ�ͼ

	$git tag v1.0		//����ǰ��֧���µı�ǩ
	$git tag 		//�鿴���б�ǩ
	
	$git config --global color.ui true	//�ı�git��ɫ








