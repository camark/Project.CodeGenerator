
ԭ�ɣ�T4ģ�治�׵��ԣ������.NET��ģ�����������ɴ���

1.NET��ģ������
  1.1NVelocity
  1.2RazorEngine

  --
  RazorEngine ��Ҫԭ�����д�����ʾ
  ��ַ��
  http://razorengine.codeplex.com/
  https://github.com/Antaris/RazorEngine
  �ο��ĵ���
  1.1����NVelocity��������Razor	http://www.cnblogs.com/huangxincheng/p/3644313.html
  1.2RazorEngine����	https://antaris.github.io/RazorEngine/ 	https://github.com/Antaris/RazorEngine
  1.3ASP.NET Razor-���	http://www.w3school.com.cn/aspnet/razor_intro.asp

  ------------------------------------------------------------------------------------------------
  д����1
      @foreach (Column c in table.Columns)
    {
        string temp = string.Format(@"
            private String {0};
            public String {1}
            {{
                get {{ return {0}; }}
                set {{ {0} = value; }}
            }}
        ", c.LowerColumnName, c.UpColumnName);

        @(temp)
    }

   д����2
   1.1ͨ��<h1><h2><h3>����������Ƕ��
   1.2
    @foreach (Column c in table.Columns)
    {
        <h1>
            private String @c.LowerColumnName;

            public String @c.UpColumnName
            {
            get { return @c.LowerColumnName; }
            set { @c.LowerColumnName = value; }
            }

        </h1>
    }
   1.3ͨ��������ɾ��<h1>

------------------------------------------------------------------------------------------------
  Dao�а����ķ�����
  1.Add
  2.DeleteById
  3.UpdateById
  4.FindById
  5.FindList
  6.FindListByPage
  7.Count