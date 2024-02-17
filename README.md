package servlet.com;
import java.io.IOException;
import java.io.PrintWriter;
import java.util.Date;

import javax.servlet.Servlet;
import javax.servlet.ServletConfig;
import javax.servlet.ServletException;
import javax.servlet.ServletRequest;
import javax.servlet.ServletResponse;

public class FirstProgramm implements Servlet {

	private ServletResponse res;

	@Override
	public void destroy() {
		// TODO Auto-generated method stub
		System.out.println("destroy call");
	}

	

	@Override
	public void init(ServletConfig arg0) throws ServletException {
		// TODO Auto-generated method stub
		System.out.println("init call");
	}

	@Override
	public void service(ServletRequest req, ServletResponse res) throws ServletException, IOException {
		// TODO Auto-generated method stub
		System.out.println("service call");
		res.setContentType("text/html");
		PrintWriter out=res.getWriter();
		out.println("welcome to the servlet");
		out.println("Today"+new Date().toString());
	}
	@Override
	public ServletConfig getServletConfig() {
		// TODO Auto-generated method stub
		return null;
	}

	@Override
	public String getServletInfo() {
		// TODO Auto-generated method stub
		return null;
	}
	
}

	

