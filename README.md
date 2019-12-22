# BankAccountProject
public class BankAccount {
	private Bank bank;
	private Person owner;
	private int balance;
	private int accountNumber;
	static int accountCounter=0;
	
	public BankAccount(Bank bank, Person owner, int balance, int accountNumber) {
		super();
		this.bank = bank;
		this.owner = owner;
		this.balance = balance;
		this.accountNumber = accountNumber;
		
	}

	public Bank getBank() {
		return bank;
	}

	public void setBank(Bank bank) {
		this.bank = bank;
	}

	public Person getOwner() {
		return owner;
	}

	public void setOwner(Person owner) {
		this.owner = owner;
	}

	public int getBalance() {
		return balance;
	}

	public void setBalance(int balance) {
		this.balance = balance;
	}

	public int getAccountNumber() {
		return accountNumber;
	}

	public void setAccountNumber(int accountNumber) {
		this.accountNumber = accountNumber;
	}
	 
	
	  //implement the  static bankAccountCounter...
	  
	public void deposit(int money)
	{
		this.setBalance(this.getBalance()+money);
	}
	public void withdraw(int money)
	{
		
		if(balance<money)
			System.out.println("Cannot withdraw " + money +" from account #"+this.accountNumber);
		else
			this.setBalance(this.getBalance()-money);
			
	}

	
	public String toString() {
		return "#"+ this.getAccountNumber()+" "+ bank.getName()+": "+ this.balance+"$ "+ "\n"+
	   "Owner Information:" + "\n" + owner.toString() + "\n";
	}
	public void interest()
	{
		if(balance<250)
		{
			balance += 15;
		}
		else if(balance>500)
		{
			balance += 35;
		}
		else
		{
			balance+=20;
		}
	}
	
	

}

