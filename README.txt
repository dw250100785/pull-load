һ�����PC���ƶ��豸������ˢ�º��������ص������ͬʱҲ֧�ֹ������ײ����غͳ�ʼ���󼴿�ʼ����
1.����js��
	<script type="text/javascript" src="dist/pull-load.min.js"></script>

2.ʹ�ã�
	new PullLoad({
        container:document.getElementById("outerScroller"),
        down:{
            distance:50,//Ĭ�Ͼ���
            enable:true,
            callback:function (end) {
                setTimeout(function () {
                    console.log("end");
                    var isEmptyData = false;
                    end(isEmptyData);
                },1500);
            }
        },
        up:{
            distance:50,//Ĭ�Ͼ��룬Ҳ�Ǵ�����div��Ĭ��g�߶�
            isScrollLoad:false,
            isInitLoad:false,
            enable:true,
            callback:function (end) {
                setTimeout(function () {
                    console.log("end");
                    var isEmptyData = false;
                    end(isEmptyData);
                },1500);
            }
        }
    });

3.up��
	up:{
		//�������������ƥ������ʾ�������ظ��࣬������ʾ�ͷż���
		distance:50,
		//������div��������Ҳ���������õ�html�ĸ���
		container:'<div class="pull-load-container"></div>',
		//��ʼ��ʱ��ʾ��html
		init:'<div class="pull-load-up"><span><span class="pull-load-up-icon"></span>�������ظ���...</span></div>',
		//����ʱ��ʾ��html
		loading:'<div class="pull-load-up loading"><span class="pull-load-up-icon"></span>������...</span></div>',
		//�ͷŵ�ʱ����ʾ��html
		release:'<div class="pull-load-up flip"><span><span class="pull-load-up-icon"></span>�ͷż���...</span></div>',
		//û�����ݵ�ʱ����ʾ��html
		emptyData:'<div class="pull-load-empty-data">û�и���������</div>',
		//�Ƿ����
		enable:true,
		//�Ƿ������div�ײ��ͼ��ء�
		isScrollLoad:false,
		//�Ƿ��ʼ����ɺ�ͼ���
		isInitLoad:false,
		//�ص�����������Ϊ���ý���Ҫִ�еĺ���
		callback:function(end){
			//δ���ص����ݵ�ʱ������Ϊtrue������Ϊfalse
			var isEmptyData = true;
			//��������и����������������Ƿ��Ѿ�û�������ˡ�
			end(isEmptyData)
		}
	}
4.down������ͬup��:
	down:{
		//�������������ƥ������ʾ�������ظ��࣬������ʾ�ͷż��أ�ͬʱҲ��Ҫ�����ĵײ�div��Ĭ�ϸ߶�
		distance:50,
		container:'<div class="pull-load-container"></div>',
		init:'<div class="pull-load-down"><span><span class="pull-load-down-icon"></span>����ˢ��...</span></div>',
		loading:'<div class="pull-load-down loading"><span class="pull-load-down-icon"></span>ˢ����...</span></div>',
		release:'<div class="pull-load-down flip"><span><span class="pull-load-down-icon"></span>�ͷ�ˢ��...</span></div>',
		emptyData:'<div class="pull-load-empty-data">û�и���������</div>',
		enable:true,
		callback:null
	}