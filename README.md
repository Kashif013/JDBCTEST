import java.sql.*;
import sun.jdbc.odbc.*;
class TestConn
{
	public static void main(String[] args)throws Exception
	{
		DriverManager.registerDriver(new Oracle.jdbc.driver.OracleDriver());

    Connection con=DriverManager.getConnection("jdbc:oracle:thin:@localhost:8080:xe","system","manager");

	Class.forName("new Oracle.jdbc.driver");

    Statement st=con.createStatement();

	String ddl= "create table Emp (id number,name varchar2(30))";
	con.Execute(dml);

	String dml="insert into Emp values (1,"Kashif")";
	con.ExecutrUpdate(dml);

	ResultSet rs=con.executeQuery("select * from emp");
     while(rs.next())
		{
		  System.out.println("First data" + rs.getInt());
		   System.out.println("Second data" + rs.getString());
		   con.close();
         }
