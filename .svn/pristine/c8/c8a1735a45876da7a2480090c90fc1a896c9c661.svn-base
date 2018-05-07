<%@ page language="java" contentType="text/html; charset=UTF-8"
	pageEncoding="UTF-8"%>
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
<script type="text/javascript" src="${pageContext.request.contextPath }/js/jquery.min.js"></script>
<title>Insert title here</title>
</head>
<body>
<form id="form">
	<table border="1" align="center">
		<th colspan="4">爬虫控制平台</th>
		<tr align="center" height="50px">
			<td width="200px">
				数据源类型
			</td>
			<td width="150px">
				模块
			</td>
			<td width="100px">
				区域
			</td>
			<td width="100px">
			</td>
		</tr>
		<tr align="center" height="50px">
			<td>
				<select name="dataSource" style="width: 120px;height: 30px;">
					<option value="Lvmama">Lvmama</option>
					<option value="Ctrip">Ctrip</option>
					<option value="Tuniu">Tuniu</option>
					<option value="Tongcheng">Tongcheng</option>
					<option value="Qunar">Quner</option>
				</select>
			</td>
			<td>
				<select name="datamodel" style="width: 90px;height: 30px;">
					<option value="Stroke">Stroke</option>
					<option value="Scenic">Scenic</option>
					<option value="Hotel">Hotel</option>
					<option value="Route">Route</option>
				</select>
			</td>
			<td>
				<select name="address" style="width: 60px;height: 30px;">
					<option value="海南">海南</option>
					<option value="上海">上海</option>
					<option value="all">全部</option>
				</select>
			</td>
			<td>
				<input id="subbutton" value="执行" type="button" style="height: 30px;">
			</td>
		</tr>
	</table>
</form>
</body>
<script type="text/javascript">
	$("#subbutton").click(function(){
		$.post("active",$("#form").serialize(),function(data){
			alert(data);
		});
	})
</script>
</html>