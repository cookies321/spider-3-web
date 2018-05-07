package cn.jj.controller;

import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.beans.factory.annotation.Value;
import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.bind.annotation.ResponseBody;

import com.holyrobot.data.Param;
import com.holyrobot.data.Params;

import cn.jj.service.IDownLoadService;
import cn.jj.service.IParseService;
import cn.jj.service.JedisClient;
import cn.jj.service.ProducerService;
import redis.clients.jedis.Jedis;


@Controller
public class ActionController {
	
	@Value("${Lvmama_Stroke_hainan}")
	private String Lvmama_Stroke_hainan;
	
	@Value("${Lvmama_Stroke_shanghai}")
	private String Lvmama_Stroke_shanghai;
	
	@Value("${Lvmama_Scenic_hainan}")
	private String Lvmama_Scenic_hainan;
	
	@Value("${Lvmama_Scenic_shanghai}")
	private String Lvmama_Scenic_shanghai;
	
	@Value("${Lvmama_Hotel_hainan}")
	private String Lvmama_Hotel_hainan;
	
	@Value("${Lvmama_Hotel_shanghai}")
	private String Lvmama_Hotel_shanghai;
	
	@Value("${Lvmama_Route_hainan}")
	private String Lvmama_Route_hainan;
	
	@Value("${Lvmama_Route_shanghai}")
	private String Lvmama_Route_shanghai;
	
	
	@Value("${Ctrip_Stroke_hainan}")
	private String Ctrip_Stroke_hainan;
	
	@Value("${Ctrip_Stroke_shanghai}")
	private String Ctrip_Stroke_shanghai;
	
	@Value("${Ctrip_Scenic_hainan}")
	private String Ctrip_Scenic_hainan;
	
	@Value("${Ctrip_Scenic_shanghai}")
	private String Ctrip_Scenic_shanghai;
	
	@Value("${Ctrip_Hotel_hainan}")
	private String Ctrip_Hotel_hainan;
	
	@Value("${Ctrip_Hotel_shanghai}")
	private String Ctrip_Hotel_shanghai;
	
	@Value("${Ctrip_Route_hainan}")
	private String Ctrip_Route_hainan;
	
	@Value("${Ctrip_Route_shanghai}")
	private String Ctrip_Route_shanghai;
	
	
	@Value("${Tuniu_Stroke_hainan}")
	private String Tuniu_Stroke_hainan;
	
	@Value("${Tuniu_Stroke_shanghai}")
	private String Tuniu_Stroke_shanghai;
	
	@Value("${Tuniu_Scenic_hainan}")
	private String Tuniu_Scenic_hainan;
	
	@Value("${Tuniu_Scenic_shanghai}")
	private String Tuniu_Scenic_shanghai;
	
	@Value("${Tuniu_Hotel_hainan}")
	private String Tuniu_Hotel_hainan;
	
	@Value("${Tuniu_Hotel_shanghai}")
	private String Tuniu_Hotel_shanghai;
	
	@Value("${Tuniu_Route_hainan}")
	private String Tuniu_Route_hainan;
	
	@Value("${Tuniu_Route_shanghai}")
	private String Tuniu_Route_shanghai;
	
	@Autowired
	private ProducerService producerService;
	
	@Autowired
	private JedisClient jedis;
	
	@RequestMapping("/active")
	@ResponseBody
	public String test(@RequestParam String dataSource,@RequestParam String datamodel,@RequestParam String address){
		//清空redis
		//jedis.flushDB();
		
		Params params = new Params();
		
		params.setCityName(address);
		
		if("Lvmama".equals(dataSource)){
			params.setDataSource(Param.LVMAMA);
			
			if("Stroke".equals(datamodel)){
				
				params.setHttpType(Param.GET);
				params.setType(Param.LVMAMA_STROKE_FIRST);
				
				if("海南".equals(address)){
					String url=Lvmama_Stroke_hainan;
					params.setUrl(url);
					params.setDataSource(Param.LVMAMA);
					params.setDestinationName("topQueue");
					producerService.sendMessage("topQueue",params);
					
				}else if("上海".equals(address)){
					String url=Lvmama_Stroke_shanghai;
					params.setUrl(url);
					params.setDataSource(Param.LVMAMA);
					params.setDestinationName("topQueue");
					producerService.sendMessage("topQueue",params);
				}
				
			}else if("Scenic".equals(datamodel)){
				params.setHttpType(Param.GET);
				params.setType(Param.LVMAMA_SCENIC_FIRST);
				
				if("海南".equals(address)){
					String url=Lvmama_Scenic_hainan;
					params.setUrl(url);
					params.setDataSource(Param.LVMAMA);
					params.setDestinationName("topQueue");
					producerService.sendMessage("topQueue",params);
					
				}else if("上海".equals(address)){
					String url=Lvmama_Scenic_shanghai;
					params.setUrl(url);
					params.setDataSource(Param.LVMAMA);
					params.setDestinationName("topQueue");
					producerService.sendMessage("topQueue",params);
				}
				
			}else if("Hotel".equals(datamodel)){
				params.setHttpType(Param.GET);
				params.setType(Param.LVMAMA_HOTEL_FIRST);
				
				if("海南".equals(address)){
					String url=Lvmama_Hotel_hainan;
					params.setUrl(url);
					params.setDataSource(Param.LVMAMA);
					params.setDestinationName("topQueue");
					producerService.sendMessage("topQueue",params);
					
				}else if("上海".equals(address)){
					String url=Lvmama_Route_hainan;
					params.setUrl(url);
					params.setDataSource(Param.LVMAMA);
					params.setDestinationName("topQueue");
					producerService.sendMessage("topQueue",params);
				}
				
			}else if("Route".equals(datamodel)){
				params.setHttpType(Param.GET);
				params.setType(Param.LVMAMA_ROUTE_FIRST);
				
				if("海南".equals(address)){
					String url=Lvmama_Route_hainan;
					params.setUrl(url);
					params.setDataSource(Param.LVMAMA);
					params.setDestinationName("topQueue");
					producerService.sendMessage("topQueue",params);
					
				}else if("上海".equals(address)){
					String url=Lvmama_Route_shanghai;
					params.setUrl(url);
					params.setDataSource(Param.LVMAMA);
					params.setDestinationName("topQueue");
					producerService.sendMessage("topQueue",params);
				}
			}
			
		}else if("Ctrip".equals(dataSource)){
			params.setDataSource(Param.CTRIP);
			
			if("Stroke".equals(datamodel)){
				params.setHttpType(Param.GET);
				params.setType(Param.CTRIP_STROKE_FIRST);
				
				if("海南".equals(address)){
					String url=Ctrip_Stroke_hainan;
					params.setUrl(url);
					params.setDataSource(Param.CTRIP);
					params.setDestinationName("topQueue");
					producerService.sendMessage("topQueue",params);
					
				}else if("上海".equals(address)){
					String url=Ctrip_Stroke_shanghai;
					params.setUrl(url);
					params.setDataSource(Param.CTRIP);
					params.setDestinationName("topQueue");
					producerService.sendMessage("topQueue",params);
				}
			}else if("Scenic".equals(datamodel)){
				params.setHttpType(Param.GET);
				params.setType(Param.CTRIP_SCENIC_FIRST);
				
				if("海南".equals(address)){
					String url=Ctrip_Scenic_hainan;
					params.setUrl(url);
					params.setDataSource(Param.CTRIP);
					params.setDestinationName("topQueue");
					producerService.sendMessage("topQueue",params);
					
				}else if("上海".equals(address)){
					String url=Ctrip_Scenic_shanghai;
					params.setUrl(url);
					params.setDataSource(Param.CTRIP);
					params.setDestinationName("topQueue");
					producerService.sendMessage("topQueue",params);
				}
			}else if("Hotel".equals(datamodel)){
				params.setHttpType(Param.GET);
				params.setType(Param.CTRIP_HOTEL_FIRST);
				
				if("海南".equals(address)){
					String url=Ctrip_Hotel_hainan;
					params.setUrl(url);
					params.setDataSource(Param.CTRIP);
					params.setDestinationName("topQueue");
					producerService.sendMessage("topQueue",params);
					
				}else if("上海".equals(address)){
					String url=Ctrip_Hotel_shanghai;
					params.setUrl(url);
					params.setDataSource(Param.CTRIP);
					params.setDestinationName("topQueue");
					producerService.sendMessage("topQueue",params);
				}
			}else if("Route".equals(datamodel)){
				params.setHttpType(Param.GET);
				params.setType(Param.CTRIP_ROUTE_FIRST);
				
				if("海南".equals(address)){
					String url=Ctrip_Route_hainan;
					params.setUrl(url);
					params.setDataSource(Param.CTRIP);
					params.setDestinationName("topQueue");
					producerService.sendMessage("topQueue",params);
					
				}else if("上海".equals(address)){
					String url=Ctrip_Route_shanghai;
					params.setUrl(url);
					params.setDataSource(Param.CTRIP);
					params.setDestinationName("topQueue");
					producerService.sendMessage("topQueue",params);
				}
			}
			
		}else if("Tuniu".equals(dataSource)){
			params.setDataSource(Param.TUNIU);
			
			if("Stroke".equals(datamodel)){
				params.setHttpType(Param.GET);
				params.setType(Param.TUNIU_STROKE_FIRST);
				
				if("海南".equals(address)){
					String url=Tuniu_Stroke_hainan;
					params.setUrl(url);
					params.setDestinationName("topQueue");
					producerService.sendMessage("topQueue",params);
					
				}else if("上海".equals(address)){
					String url=Tuniu_Stroke_shanghai;
					params.setUrl(url);
					params.setDestinationName("topQueue");
					producerService.sendMessage("topQueue",params);
				}
			}else if("Scenic".equals(datamodel)){
				params.setHttpType(Param.GET);
				params.setType(Param.TUNIU_SCENIC_FIRST);
				
				if("海南".equals(address)){
					String url=Tuniu_Scenic_hainan;
					params.setUrl(url);
					params.setDestinationName("topQueue");
					producerService.sendMessage("topQueue",params);
					
				}else if("上海".equals(address)){
					String url=Tuniu_Scenic_shanghai;
					params.setUrl(url);
					params.setDestinationName("topQueue");
					producerService.sendMessage("topQueue",params);
				}
			}else if("Hotel".equals(datamodel)){
				params.setHttpType(Param.GET);
				params.setType(Param.TUNIU_HOTEL_FIRST);
				
				if("海南".equals(address)){
					String url=Tuniu_Hotel_hainan;
					params.setUrl(url);
					params.setDestinationName("topQueue");
					producerService.sendMessage("topQueue",params);
					
				}else if("上海".equals(address)){
					String url=Tuniu_Hotel_shanghai;
					params.setUrl(url);
					params.setDestinationName("topQueue");
					producerService.sendMessage("topQueue",params);
				}
			}else if("Route".equals(datamodel)){
				params.setHttpType(Param.GET);
				params.setType(Param.TUNIU_ROUTE_FIRST);
				
				if("海南".equals(address)){
					String url=Tuniu_Route_hainan;
					params.setUrl(url);
					params.setDestinationName("topQueue");
					producerService.sendMessage("topQueue",params);
					
				}else if("上海".equals(address)){
					String url=Tuniu_Route_shanghai;
					params.setUrl(url);
					params.setDestinationName("topQueue");
					producerService.sendMessage("topQueue",params);
				}
			}
			
		}else if("Tongcheng".equals(dataSource)){
			if("Stroke".equals(datamodel)){
				
			}else if("Scenic".equals(datamodel)){
				
			}else if("Hotel".equals(datamodel)){
				
			}else if("Route".equals(datamodel)){
				
			}
			
		}else if("Qunar".equals(dataSource)){
			if("Stroke".equals(datamodel)){
				
			}else if("Scenic".equals(datamodel)){
				
			}else if("Hotel".equals(datamodel)){
				
			}else if("Route".equals(datamodel)){
				
			}
		}
		return "success";
	}
	

}
