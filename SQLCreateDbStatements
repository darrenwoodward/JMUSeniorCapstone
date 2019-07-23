
drop table if exists PeerTransaction;
drop table if exists Category;
drop table if exists Value;
drop table if exists EmployeeTeam;
drop table if exists Team;
drop table if exists MoneyTransaction;

drop table if exists RewardProviderPool;
drop table if exists GiftCardReceipt;
drop table if exists Person;
drop table if exists GiftCard;

drop table if exists BusinessEntity;
drop table if exists RewardProvider;

USE [FinalProject]
GO

USE [FinalProject]
GO
/****** Object:  Table [dbo].[Team]    Script Date: 4/12/2018 2:47:36 PM ******/
SET ANSI_NULLS ON
GO

SET QUOTED_IDENTIFIER ON
GO

CREATE TABLE [dbo].[Team](
	[TeamID] [int] IDENTITY(1,1) NOT NULL,
	[CreatorID] [int] NOT NULL,
	[TeamName] [varchar](20) NOT NULL,
	[TeamDescription] [varchar](250) NOT NULL,
	[StartDate] [date] NOT NULL,
	[EndDate] [date] NULL,
	[LastUpdated] [date] NOT NULL,
	[LastUpdatedBy] [varchar](20) NOT NULL,
	[Status] [int] NOT NULL,
 CONSTRAINT [PK_Team] PRIMARY KEY CLUSTERED 
(
	[TeamID] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY]
GO
USE [FinalProject]
GO

/****** Object:  Table [dbo].[BusinessEntity]    Script Date: 4/12/2018 2:48:27 PM ******/
SET ANSI_NULLS ON
GO

SET QUOTED_IDENTIFIER ON
GO

CREATE TABLE [dbo].[BusinessEntity](
	[BusinessEntityID] [int] IDENTITY(1,1) NOT NULL,
	[BusinessEntityName] [varchar](50) NULL,
	[PhoneNumber] [varchar](25) NULL,
	[Email] [varchar](100) NULL,
	[LastUpdated] [date] NOT NULL,
	[LastUpdatedBy] [varchar](20) NULL,
 CONSTRAINT [PK_BusinessEntity] PRIMARY KEY CLUSTERED 
(
	[BusinessEntityID] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY]
GO


USE [FinalProject]
GO

/****** Object:  Table [dbo].[Category]    Script Date: 4/12/2018 2:49:04 PM ******/
SET ANSI_NULLS ON
GO

SET QUOTED_IDENTIFIER ON
GO

CREATE TABLE [dbo].[Category](
	[CategoryID] [int] IDENTITY(1,1) NOT NULL,
	[Title] [varchar](20) NOT NULL,
	[LastUpdated] [date] NOT NULL,
	[LastUpdatedBy] [varchar](20) NOT NULL,
 CONSTRAINT [PK_Category] PRIMARY KEY CLUSTERED 
(
	[CategoryID] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY]
GO


USE [FinalProject]
GO

/****** Object:  Table [dbo].[Value]    Script Date: 4/12/2018 2:50:09 PM ******/
SET ANSI_NULLS ON
GO

SET QUOTED_IDENTIFIER ON
GO

CREATE TABLE [dbo].[Value](
	[ValueID] [int] IDENTITY(1,1) NOT NULL,
	[ValueName] [varchar](50) NOT NULL,
	[ValueDescription] [varchar](250) NOT NULL,
	[LastUpdated] [date] NOT NULL,
	[LastUpdatedBy] [varchar](20) NOT NULL,
	[BusinessEntityID] [int] NOT NULL,
 CONSTRAINT [PK_Value] PRIMARY KEY CLUSTERED 
(
	[ValueID] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY]
GO

ALTER TABLE [dbo].[Value]  WITH CHECK ADD  CONSTRAINT [FK_Value_BusinessEntity] FOREIGN KEY([BusinessEntityID])
REFERENCES [dbo].[BusinessEntity] ([BusinessEntityID])
GO

ALTER TABLE [dbo].[Value] CHECK CONSTRAINT [FK_Value_BusinessEntity]
GO



USE [FinalProject]
GO

/****** Object:  Table [dbo].[Person]    Script Date: 4/12/2018 2:51:10 PM ******/
SET ANSI_NULLS ON
GO

SET QUOTED_IDENTIFIER ON
GO

CREATE TABLE [dbo].[Person](
	[PersonID] [int] IDENTITY(1,1) NOT NULL,
	[FirstName] [varchar](20) NOT NULL,
	[LastName] [varchar](20) NOT NULL,
	[MI] [char](1) NULL,
	[NickName] [varchar](20) NULL,
	[E-mail] [varchar](100) NULL,
	[Position] [varchar](20) NOT NULL,
	[Password] [varchar](50) NOT NULL,
	[UserName] [varchar](100) NULL,
	[PointsBalance] [money] NOT NULL,
	[PendingPoints] [money] NOT NULL,
	[LastUpdated] [date] NOT NULL,
	[LastUpdatedBy] [varchar](20) NOT NULL,
	[ProfilePicture] [image] NULL,
	[loginCount] [int] NOT NULL,
	[PageLand] [varchar](50) NULL,
	[Anonymous] [varchar](5) NULL,
	[TempName] [varchar](25) NULL,
	[BusinessEntityID] [int] NOT NULL,
	[Status] [varchar](50) NULL,
 CONSTRAINT [PK_Person] PRIMARY KEY CLUSTERED 
(
	[PersonID] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY] TEXTIMAGE_ON [PRIMARY]
GO

ALTER TABLE [dbo].[Person]  WITH CHECK ADD  CONSTRAINT [FK_Person_Business] FOREIGN KEY([BusinessEntityID])
REFERENCES [dbo].[BusinessEntity] ([BusinessEntityID])
GO

ALTER TABLE [dbo].[Person] CHECK CONSTRAINT [FK_Person_Business]
GO


USE [FinalProject]
GO

/****** Object:  Table [dbo].[RewardProvider]    Script Date: 4/12/2018 2:52:20 PM ******/
SET ANSI_NULLS ON
GO

SET QUOTED_IDENTIFIER ON
GO

CREATE TABLE [dbo].[RewardProvider](
	[RewardProviderID] [int] IDENTITY(1,1) NOT NULL,
	[RewardProviderName] [varchar](40) NOT NULL,
	[PhoneNumber] [varchar](20) NOT NULL,
	[Email] [varchar](100) NULL,
	[Username] [varchar](100) NULL,
	[Password] [varchar](50) NOT NULL,
	[Balance] [money] NULL,
	[LastUpdated] [date] NOT NULL,
	[LastUpdatedBy] [varchar](20) NOT NULL,
	[ProfilePicture] [image] NULL,
 CONSTRAINT [PK_RewardProvider] PRIMARY KEY CLUSTERED 
(
	[RewardProviderID] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY] TEXTIMAGE_ON [PRIMARY]
GO



USE [FinalProject]
GO

/****** Object:  Table [dbo].[RewardProviderPool]    Script Date: 4/12/2018 2:52:40 PM ******/
SET ANSI_NULLS ON
GO

SET QUOTED_IDENTIFIER ON
GO

CREATE TABLE [dbo].[RewardProviderPool](
	[BusinessEntityID] [int] NOT NULL,
	[RewardProviderID] [int] NOT NULL,
	[Status] [varchar](50) NULL,
	[LastUpdated] [date] NOT NULL,
	[LastUpdatedBy] [varchar](20) NOT NULL,
 CONSTRAINT [PK_RewardProviderPool] PRIMARY KEY CLUSTERED 
(
	[BusinessEntityID] ASC,
	[RewardProviderID] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY]
GO

ALTER TABLE [dbo].[RewardProviderPool]  WITH CHECK ADD  CONSTRAINT [FK_RewardProviderPool_BusinessEntity] FOREIGN KEY([BusinessEntityID])
REFERENCES [dbo].[BusinessEntity] ([BusinessEntityID])
GO

ALTER TABLE [dbo].[RewardProviderPool] CHECK CONSTRAINT [FK_RewardProviderPool_BusinessEntity]
GO

ALTER TABLE [dbo].[RewardProviderPool]  WITH CHECK ADD  CONSTRAINT [FK_RewardProviderPool_RewardProvider] FOREIGN KEY([RewardProviderID])
REFERENCES [dbo].[RewardProvider] ([RewardProviderID])
GO

ALTER TABLE [dbo].[RewardProviderPool] CHECK CONSTRAINT [FK_RewardProviderPool_RewardProvider]
GO


USE [FinalProject]
GO

/****** Object:  Table [dbo].[EmployeeTeam]    Script Date: 4/12/2018 2:54:26 PM ******/
SET ANSI_NULLS ON
GO

SET QUOTED_IDENTIFIER ON
GO

CREATE TABLE [dbo].[EmployeeTeam](
	[PersonID] [int] NOT NULL,
	[TeamID] [int] NOT NULL,
	[JoinDate] [date] NOT NULL,
	[LeaveDate] [date] NULL,
	[LastUpdated] [date] NOT NULL,
	[LastUpdatedBy] [varchar](20) NOT NULL,
 CONSTRAINT [PK_EmployeeTeam] PRIMARY KEY CLUSTERED 
(
	[PersonID] ASC,
	[TeamID] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY]
GO

ALTER TABLE [dbo].[EmployeeTeam]  WITH CHECK ADD  CONSTRAINT [FK_EmployeeTeam_Person] FOREIGN KEY([PersonID])
REFERENCES [dbo].[Person] ([PersonID])
GO

ALTER TABLE [dbo].[EmployeeTeam] CHECK CONSTRAINT [FK_EmployeeTeam_Person]
GO

ALTER TABLE [dbo].[EmployeeTeam]  WITH CHECK ADD  CONSTRAINT [FK_EmployeeTeam_Team] FOREIGN KEY([TeamID])
REFERENCES [dbo].[Team] ([TeamID])
GO

ALTER TABLE [dbo].[EmployeeTeam] CHECK CONSTRAINT [FK_EmployeeTeam_Team]
GO


USE [FinalProject]
GO

/****** Object:  Table [dbo].[GiftCard]    Script Date: 4/12/2018 2:56:28 PM ******/
SET ANSI_NULLS ON
GO

SET QUOTED_IDENTIFIER ON
GO

CREATE TABLE [dbo].[GiftCard](
	[GiftCardID] [int] IDENTITY(1,1) NOT NULL,
	[RewardProviderID] [int] NOT NULL,
	[Value] [money] NULL,
	[Description] [varchar](250) NULL,
	[DatePosted] [date] NOT NULL,
	[Status] [varchar](20) NOT NULL,
	[DateRemoved] [date] NULL,
	[LastUpdated] [date] NOT NULL,
	[LastUpdatedBy] [varchar](20) NOT NULL,
	[VoucherNumber] [varchar](100) NULL,
	[ImageGC] [image] NULL,
	[BusinessEntityID] [int] NOT NULL,
 CONSTRAINT [PK_GiftCard] PRIMARY KEY CLUSTERED 
(
	[GiftCardID] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY] TEXTIMAGE_ON [PRIMARY]
GO

ALTER TABLE [dbo].[GiftCard]  WITH CHECK ADD  CONSTRAINT [FK_GiftCard_BusinessEntityID] FOREIGN KEY([BusinessEntityID])
REFERENCES [dbo].[BusinessEntity] ([BusinessEntityID])
GO

ALTER TABLE [dbo].[GiftCard] CHECK CONSTRAINT [FK_GiftCard_BusinessEntityID]
GO

ALTER TABLE [dbo].[GiftCard]  WITH CHECK ADD  CONSTRAINT [FK_GiftCard_RewardProviderID] FOREIGN KEY([RewardProviderID])
REFERENCES [dbo].[RewardProvider] ([RewardProviderID])
GO

ALTER TABLE [dbo].[GiftCard] CHECK CONSTRAINT [FK_GiftCard_RewardProviderID]
GO

USE [FinalProject]
GO

/****** Object:  Table [dbo].[GiftCardReceipt]    Script Date: 4/12/2018 2:56:56 PM ******/
SET ANSI_NULLS ON
GO

SET QUOTED_IDENTIFIER ON
GO

CREATE TABLE [dbo].[GiftCardReceipt](
	[GiftCardReceiptID] [int] IDENTITY(1,1) NOT NULL,
	[GiftCardID] [int] NOT NULL,
	[PersonID] [int] NOT NULL,
	[PurchaseDate] [date] NOT NULL,
	[LastUpdated] [date] NOT NULL,
	[LastUpdatedBy] [varchar](20) NOT NULL,
	[ConfirmationNumber] [int] NULL,
 CONSTRAINT [PK_GiftCardReceipt] PRIMARY KEY CLUSTERED 
(
	[GiftCardReceiptID] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY]
GO

ALTER TABLE [dbo].[GiftCardReceipt]  WITH CHECK ADD  CONSTRAINT [FK_GiftCardReceip_Person] FOREIGN KEY([PersonID])
REFERENCES [dbo].[Person] ([PersonID])
GO

ALTER TABLE [dbo].[GiftCardReceipt] CHECK CONSTRAINT [FK_GiftCardReceip_Person]
GO

ALTER TABLE [dbo].[GiftCardReceipt]  WITH CHECK ADD  CONSTRAINT [FK_GiftCardReceipt_GiftCard] FOREIGN KEY([GiftCardID])
REFERENCES [dbo].[GiftCard] ([GiftCardID])
GO

ALTER TABLE [dbo].[GiftCardReceipt] CHECK CONSTRAINT [FK_GiftCardReceipt_GiftCard]
GO

USE [FinalProject]
GO

/****** Object:  Table [dbo].[PeerTransaction]    Script Date: 4/12/2018 2:57:44 PM ******/
SET ANSI_NULLS ON
GO

SET QUOTED_IDENTIFIER ON
GO

CREATE TABLE [dbo].[PeerTransaction](
	[TransactionID] [int] IDENTITY(1,1) NOT NULL,
	[PointsAmount] [money] NOT NULL,
	[Date] [date] NOT NULL,
	[EventDescription] [varchar](250) NOT NULL,
	[LastUpdated] [date] NOT NULL,
	[LastUpdatedBy] [varchar](20) NOT NULL,
	[ReceiverID] [int] NOT NULL,
	[RewarderID] [int] NOT NULL,
	[CategoryID] [int] NOT NULL,
	[ValueID] [int] NOT NULL,
 CONSTRAINT [PK_PeerTransaction] PRIMARY KEY CLUSTERED 
(
	[TransactionID] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY]
GO

ALTER TABLE [dbo].[PeerTransaction]  WITH CHECK ADD  CONSTRAINT [FK_PeerTransaction_Category] FOREIGN KEY([CategoryID])
REFERENCES [dbo].[Category] ([CategoryID])
GO

ALTER TABLE [dbo].[PeerTransaction] CHECK CONSTRAINT [FK_PeerTransaction_Category]
GO

ALTER TABLE [dbo].[PeerTransaction]  WITH CHECK ADD  CONSTRAINT [FK_PeerTransaction_Person] FOREIGN KEY([ReceiverID])
REFERENCES [dbo].[Person] ([PersonID])
GO

ALTER TABLE [dbo].[PeerTransaction] CHECK CONSTRAINT [FK_PeerTransaction_Person]
GO

ALTER TABLE [dbo].[PeerTransaction]  WITH CHECK ADD  CONSTRAINT [FK_PeerTransaction_Person1] FOREIGN KEY([RewarderID])
REFERENCES [dbo].[Person] ([PersonID])
GO

ALTER TABLE [dbo].[PeerTransaction] CHECK CONSTRAINT [FK_PeerTransaction_Person1]
GO

ALTER TABLE [dbo].[PeerTransaction]  WITH CHECK ADD  CONSTRAINT [FK_PeerTransaction_Value] FOREIGN KEY([ValueID])
REFERENCES [dbo].[Value] ([ValueID])
GO

ALTER TABLE [dbo].[PeerTransaction] CHECK CONSTRAINT [FK_PeerTransaction_Value]
GO


USE [FinalProject]
GO

/****** Object:  Table [dbo].[MoneyTransaction]    Script Date: 4/12/2018 3:01:04 PM ******/
SET ANSI_NULLS ON
GO

SET QUOTED_IDENTIFIER ON
GO

CREATE TABLE [dbo].[MoneyTransaction](
	[MoneyTransactionID] [int] IDENTITY(1,1) NOT NULL,
	[Date] [date] NOT NULL,
	[TotalAmount] [money] NOT NULL,
	[TransactionAmount] [money] NOT NULL,
	[LastUpdated] [date] NOT NULL,
	[LastUpdatedBy] [varchar](20) NOT NULL,
	[PersonID] [int] NOT NULL,
 CONSTRAINT [PK_MoneyTransaction] PRIMARY KEY CLUSTERED 
(
	[MoneyTransactionID] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY]
GO

ALTER TABLE [dbo].[MoneyTransaction]  WITH CHECK ADD  CONSTRAINT [FK_MoneyTransaction_Person] FOREIGN KEY([PersonID])
REFERENCES [dbo].[Person] ([PersonID])
GO

ALTER TABLE [dbo].[MoneyTransaction] CHECK CONSTRAINT [FK_MoneyTransaction_Person]
GO


create trigger reward_points on peertransaction
after insert 
as
begin
declare 
@ReceiverID int,
@RewardAmount int
select @ReceiverID=(select ReceiverID from inserted)
select @RewardAmount=(select PointsAmount from inserted)
update Person           
     set PointsBalance=PointsBalance+@RewardAmount
	 where PersonID=@ReceiverID
	 update person
	 set PointsBalance=PointsBalance-@RewardAmount
	 where Position='CEO'  
	
	
end 
go
  create procedure login_count @UserName varchar(20)
 as begin 
 set nocount on;
update [dbo].[Person] SET loginCount = loginCount+1 WHERE username= @username
		   end
		   go

create trigger update_points on [MoneyTransaction]
after insert 
as
begin
declare 
@ReceiverID int,
@CashAmount int
select @ReceiverID=(select PersonID from inserted)
select @CashAmount=(select TransactionAmount from inserted)
update Person           
     set PointsBalance=PointsBalance+@CashAmount
	 where PersonID=@ReceiverID
end
go
create trigger add_creator on [Team]
after insert 
as
begin
declare 
@creatorID int,
@StartDate date,
@LastUpdated date,
@LastUpdatedBy Varchar(20)
select @creatorID=(select CreatorID from inserted)
select @StartDate=(select StartDate from inserted)
select @LastUpdated=(select LastUpdated from inserted)
select @LastUpdatedBy=(select LastUpdatedBy from inserted)
INSERT INTO [dbo].[EmployeeTeam]
           ([PersonID]
           ,[TeamID]
           ,[JoinDate]
           ,[LastUpdated]
           ,[LastUpdatedBy])
     VALUES
           (@creatorID
           ,(Select max(teamID) from team)
           ,@StartDate
           ,@LastUpdated
           ,@LastUpdatedBy)
end
go
create trigger [default_pic] on [dbo].[Person]
after insert 
as
begin
declare 
@PersonID int
select @PersonID=(select PersonID from inserted)
UPDATE [Person] set [ProfilePicture]= (select [ProfilePicture] from Person where Personid=1)
where PersonID=@PersonID
end
go





INSERT INTO [dbo].[BusinessEntity]
           ([BusinessEntityName]
           ,[PhoneNumber]
           ,[Email]
           ,[LastUpdated]
           ,[LastUpdatedBy])
     VALUES
           ('NIT Consulting'
           ,'7038447888'
           ,'NIT@gmail.com'
           ,'2018-1-1'
           ,'ADMIN')
GO


INSERT INTO [dbo].[BusinessEntity]
           ([BusinessEntityName]
           ,[PhoneNumber]
           ,[Email]
           ,[LastUpdated]
           ,[LastUpdatedBy])
     VALUES
           ('Elk Logistics'
           ,'7034447888'
           ,'Logistic@gmail.com'
           ,'2018-1-1'
           ,'ADMIN')
GO

INSERT INTO [dbo].[BusinessEntity]
           ([BusinessEntityName]
           ,[PhoneNumber]
           ,[Email]
           ,[LastUpdated]
           ,[LastUpdatedBy])
     VALUES
           ('Elk Trucking'
           ,'7034447888'
           ,'Trucking@gmail.com'
           ,'2018-2-1'
           ,'ADMIN')
GO



INSERT INTO [dbo].[Category]
           ([Title]
           ,[LastUpdated]
           ,[LastUpdatedBy])
     VALUES
           ('Creative'
           ,'2018-2-7'
           ,'Tatyana')
GO
INSERT INTO [dbo].[Category]
           ([Title]
           ,[LastUpdated]
           ,[LastUpdatedBy])
     VALUES
           ('Distinguished'
           ,'2018-2-7'
           ,'Xubo Wu')
GO
INSERT INTO [dbo].[Category]
           ([Title]
           ,[LastUpdated]
           ,[LastUpdatedBy])
     VALUES
           ('Exceptional'
           ,'2018-2-7'
           ,'Xubo Wu')
GO
INSERT INTO [dbo].[Category]
           ([Title]
           ,[LastUpdated]
           ,[LastUpdatedBy])
     VALUES
           ('Fresh Approach'
           ,'2018-2-7'
           ,'Xubo Wu')
GO
INSERT INTO [dbo].[Category]
           ([Title]
           ,[LastUpdated]
           ,[LastUpdatedBy])
     VALUES
           ('Superior'
           ,'2018-2-7'
           ,'Xubo Wu')
GO
INSERT INTO [dbo].[Category]
           ([Title]
           ,[LastUpdated]
           ,[LastUpdatedBy])
     VALUES
           ('Ingenious'
           ,'2018-2-7'
           ,'Xubo Wu')
GO
INSERT INTO [dbo].[Category]
           ([Title]
           ,[LastUpdated]
           ,[LastUpdatedBy])
     VALUES
           ('Incomparable'
           ,'2018-2-7'
           ,'Xubo Wu')
GO
INSERT INTO [dbo].[Category]
           ([Title]
           ,[LastUpdated]
           ,[LastUpdatedBy])
     VALUES
           ('Outstanding'
           ,'2018-2-7'
           ,'Xubo Wu')

GO
INSERT INTO [dbo].[Category]
           ([Title]
           ,[LastUpdated]
           ,[LastUpdatedBy])
     VALUES
           ('Surprising'
           ,'2018-2-7'
           ,'Xubo Wu')
GO
INSERT INTO [dbo].[Category]
           ([Title]
           ,[LastUpdated]
           ,[LastUpdatedBy])
     VALUES
           ('Symbolic'
           ,'2018-2-7'
           ,'Xubo Wu')

GO
INSERT INTO [dbo].[Category]
           ([Title]
           ,[LastUpdated]
           ,[LastUpdatedBy])
     VALUES
           ('Unexpected'
           ,'2018-2-7'
           ,'Xubo Wu')

GO
INSERT INTO [dbo].[Value]
           ([ValueName]
           ,[ValueDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
,[BusinessEntityID]
)
     VALUES
           ('Community Service'
           ,'well being of team members'
           ,'2018-2-7'
           ,'Tatyana'
,2)
GO

INSERT INTO [dbo].[Value]
           ([ValueName]
           ,[ValueDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
,[BusinessEntityID]
)
     VALUES
           ('Health'
           ,'well being of team members'
           ,'2018-2-7'
           ,'Tatyana'
,2)
GO
INSERT INTO [dbo].[Value]
           ([ValueName]
           ,[ValueDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
,[BusinessEntityID]
)
     VALUES
           ('Well Being and Safety of Team Members'
           ,'the process of making changes to reduce injuries '
           ,'2018-2-7'
           ,'Tatyana'
,3)
GO
INSERT INTO [dbo].[Value]
           ([ValueName]
           ,[ValueDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
,[BusinessEntityID]
)
     VALUES
           ('Attracting New Customers'
           ,'the process of creating an irresistible offer'
           ,'2018-2-7'
           ,'Tatyana'
,2)
GO
INSERT INTO [dbo].[Value]
           ([ValueName]
           ,[ValueDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
,[BusinessEntityID]
)
     VALUES
           ('Community Involvement'
           ,'the process of working with the community to open up opportunities for increased safety, awareness and prevention. '
           ,'2018-2-7'
           ,'Tatyana'
,3)
GO

INSERT INTO [dbo].[Value]
           ([ValueName]
           ,[ValueDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
,[BusinessEntityID]
)
     VALUES
           ('Customer Service'
           ,'assistance and advice provided to the buyers'
           ,'2018-2-7'
           ,'Tatyana'
,2)
GO
INSERT INTO [dbo].[Value]
           ([ValueName]
           ,[ValueDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
,[BusinessEntityID]
)
     VALUES
           ('Process Improvement Initiatives'
           ,'continual improvement of process productivity'
           ,'2018-2-7'
           ,'Tatyana'
,3)
GO
INSERT INTO [dbo].[Value]
           ([ValueName]
           ,[ValueDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
,[BusinessEntityID]
)
     VALUES
           ('Leadership Development'
           ,'a program or activity that makes people become better leaders'
           ,'2018-2-7'
           ,'Tatyana'
,2)
GO

INSERT INTO [dbo].[Value]
           ([ValueName]
           ,[ValueDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
,[BusinessEntityID]
)
     VALUES
           ('Mentoring'
           ,'advise or train'
           ,'2018-2-7'
           ,'Tatyana'
,3)
GO

INSERT INTO [dbo].[Value]
           ([ValueName]
           ,[ValueDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
,[BusinessEntityID]
)
     VALUES
           ('Team Building'
           ,'the action or process of causing a group of people to work together effectively as a team'
           ,'2018-2-7'
           ,'Tatyana'
,2)
GO

INSERT INTO [dbo].[Value]
           ([ValueName]
           ,[ValueDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
,[BusinessEntityID]
)
     VALUES
           ('Education'
           ,'the process of educating community'
           ,'2018-2-7'
           ,'Tatyana'
,3
)
GO


INSERT INTO [dbo].[Person]
           ([FirstName]
           ,[LastName]
           ,[MI]
           ,[NickName]
           ,[E-mail]
           ,[Position]
           ,[Password]
           ,[UserName]
           ,[PointsBalance]
           ,[PendingPoints]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ProfilePicture]
           ,[loginCount]
           ,[PageLand]
           ,[Anonymous]
           ,[TempName]
           ,[BusinessEntityID]
,[Status])
     VALUES
           ('Darren'
           ,'Woodward'
           ,null
	    ,NULL
           ,'darrenwoodwarda@gmail.com'
           ,'CEO'
           ,'ByZws4MxTiQ2tvH1G59b6ntF1cIYPQ=='
           ,'CEO'
           ,0
           ,0
           ,'2018-2-7'
           ,'Tatyana'
           , null
	   ,1
   ,1
   ,null
   ,null,
   2,
'Active')
GO

INSERT INTO [dbo].[Person]
           ([FirstName]
           ,[LastName]
           ,[MI]
           ,[NickName]
           ,[E-mail]
           ,[Position]
           ,[Password]
           ,[UserName]
           ,[PointsBalance]
           ,[PendingPoints]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ProfilePicture]
           ,[loginCount]
           ,[PageLand]
           ,[Anonymous]
           ,[TempName]
           ,[BusinessEntityID]
,[Status])

     VALUES
           ('Xubo'
           ,'Wu'
           ,NULL
     ,NULL

           ,'wu2xx@dukes.jmu.edu'
           ,'EMPLOYEE'
           ,'L3FPQ+dLnnzJfxw+ZsJmuq+v4sSPNZc='
           ,'javauser'
           ,0
           ,0
           ,'2018-2-7'
           ,'Tatyana'
           ,NULL
	   ,1
   ,1
   ,null
   ,null,
   2,
   'Active')
GO



INSERT INTO [dbo].[Person]
           ([FirstName]
           ,[LastName]
           ,[MI]
           ,[NickName]
           ,[E-mail]
           ,[Position]
           ,[Password]
           ,[UserName]
           ,[PointsBalance]
           ,[PendingPoints]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ProfilePicture]
           ,[loginCount]
           ,[PageLand]
           ,[Anonymous]
           ,[TempName]
           ,[BusinessEntityID]
		   ,[Status])
     VALUES
           ('Carol'
            ,'Kuai'
		,NULL
,NULL
            ,'ydykl1222@gmail.com'
			,'EMPLOYEE'
			,'ypVa+7SiHA+hsJFNFBzxAuSKR9o='
			,'Carol'
			,0
			,0
			,'2018-02-25'
           ,'Tatyana'
           ,NULL
	   ,1
   ,1
          ,null
          ,null,
          2
		  ,'Active')
			GO
	
INSERT INTO [dbo].[Person]
           ([FirstName]
           ,[LastName]
           ,[MI]
           ,[NickName]
           ,[E-mail]
           ,[Position]
           ,[Password]
           ,[UserName]
           ,[PointsBalance]
           ,[PendingPoints]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ProfilePicture]
           ,[loginCount]
           ,[PageLand]
           ,[Anonymous]
           ,[TempName]
           ,[BusinessEntityID]
		   ,[Status])
     VALUES
           ('Tatyana'
           ,'Syutkina'
	       ,NULL
,NULL
             ,'syutkina.tatyana@gmail.com'
,'EMPLOYEE'
,'n2zGifHVUoRUdfAwuleJPqmu4r84'
,'Tatyana'
,0
,0
,'2017-02-12'
             ,'Tatyana'
              ,NULL
	       ,1
,1
,null
,null,
2
,'Active')
GO
INSERT INTO [dbo].[Person]
           ([FirstName]
           ,[LastName]
           ,[MI]
           ,[NickName]
           ,[E-mail]
           ,[Position]
           ,[Password]
           ,[UserName]
           ,[PointsBalance]
           ,[PendingPoints]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ProfilePicture]
           ,[loginCount]
           ,[PageLand]
           ,[Anonymous]
           ,[TempName]
           ,[BusinessEntityID]
		   ,[Status])
     VALUES
('Hila'
,'Pridan'
,null
,NULL
,'Hila@gmail.com'
,'EMPLOYEE'
,'BEZws4MxTiQ2tvH1G59b6ntF1cIYT'
,'Hila'
,0
,0
,'2018-2-7'
,'Tatyana'
,NULL
,1
,1
,null
,null,
3
,'Active')
GO

  INSERT INTO [dbo].[Person]
           ([FirstName]
           ,[LastName]
           ,[MI]
           ,[NickName]
           ,[E-mail]
           ,[Position]
           ,[Password]
           ,[UserName]
           ,[PointsBalance]
           ,[PendingPoints]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ProfilePicture]
           ,[loginCount]
           ,[PageLand]
           ,[Anonymous]
           ,[TempName]
           ,[BusinessEntityID]
		   ,[Status])
     VALUES

('Pratic'
,'KC'
,null
,NULL
,'kc.pratic7@gmail.com'
,'EMPLOYEE'
,'CDB/rRMimVxpIYkG1daWDHZZnAE='
,'Pratic'
,0
,0
,'2018-2-7'
,'Tatyana'
,NULL
,1
,1
,null
,null,
3
,'Active')
GO

  INSERT INTO [dbo].[Person]
           ([FirstName]
           ,[LastName]
           ,[MI]
           ,[NickName]
           ,[E-mail]
           ,[Position]
           ,[Password]
           ,[UserName]
           ,[PointsBalance]
           ,[PendingPoints]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ProfilePicture]
           ,[loginCount]
           ,[PageLand]
           ,[Anonymous]
           ,[TempName]
           ,[BusinessEntityID]
		   ,[Status])
     
VALUES
('Jorge'
,'C'
,null
,NULL
,'Jorge@gmail.com'
,'EMPLOYEE'
,'wwPK7vMaB3QOZxC/HxVwyjyO3qkGug=='
,'Jorge'
,0
,0
,'2018-2-7'
,'Tatyana'
,NULL
,1
,1
,null
,null,
3
,'Active')
GO
  INSERT INTO [dbo].[Person]
           ([FirstName]
           ,[LastName]
           ,[MI]
           ,[NickName]
           ,[E-mail]
           ,[Position]
           ,[Password]
           ,[UserName]
           ,[PointsBalance]
           ,[PendingPoints]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ProfilePicture]
           ,[loginCount]
           ,[PageLand]
           ,[Anonymous]
           ,[TempName]
           ,[BusinessEntityID]
		   ,[Status])
     
VALUES
('ADMIN'
,'ADMIN'
,null
,NULL
,' wodwarda@dukes.jmu.edu'
,'ADMIN'
,'/RxmXitp9SGXc4FVZ8EfFMBLyQSIxQ=='
,'ADMIN'
,0
,0
,'2018-2-7'
,'ADMIN'
,NULL
,1
,1
,null
,null,
1
,'Active')
GO
INSERT INTO [dbo].[MoneyTransaction]
           ([Date]
           ,[TotalAmount]
           ,[TransactionAmount]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[PersonID])
     VALUES
           ('2018-2-27'
           ,5000
           ,5000
           ,'2018-2-27'
           ,'ADMIN'
           ,1)
GO


  INSERT INTO [dbo].[PeerTransaction]
           ([PointsAmount]
           ,[Date]
           ,[EventDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ReceiverID]
           ,[RewarderID]
           ,[CategoryID]
           ,[ValueID]
		)

     VALUES
           (25.00
           ,'2017-02-25'
           ,'event was held in the hospital'
           ,'2017-02-25'
           ,'Tatyana'
           ,4
           ,3
           ,1
           ,1
	)

INSERT INTO [dbo].[PeerTransaction]
           ([PointsAmount]
           ,[Date]
           ,[EventDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ReceiverID]
           ,[RewarderID]
           ,[CategoryID]
           ,[ValueID]
		)

     VALUES
           (10.00
           ,'2018-02-25'
           ,'event was held in the hospital'
           ,'2018-02-25'
           ,'Tatyana'
           ,3
           ,4
           ,2
           ,4
	)
GO
INSERT INTO [dbo].[PeerTransaction]
           ([PointsAmount]
           ,[Date]
           ,[EventDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ReceiverID]
           ,[RewarderID]
           ,[CategoryID]
           ,[ValueID])

     VALUES
           (10.00
           ,'2018-02-25'
           ,'event was held in the office'
           ,'2018-02-25'
           ,'Tatyana'
           ,2
           ,4
           ,3
           ,9)
GO

INSERT INTO [dbo].[PeerTransaction]
           ([PointsAmount]
           ,[Date]
           ,[EventDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ReceiverID]
           ,[RewarderID]
           ,[CategoryID]
           ,[ValueID])

     VALUES
           (15.00
           ,'2017-06-25'
           ,'event was based on leadership development'
           ,'2017-06-25'
           ,'XUBO'
           ,4
           ,3
           ,4
           ,7)
GO

INSERT INTO [dbo].[PeerTransaction]
           ([PointsAmount]
           ,[Date]
           ,[EventDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ReceiverID]
           ,[RewarderID]
           ,[CategoryID]
           ,[ValueID])

     VALUES
           (15.00
           ,'2017-06-25'
           ,'event was based on choosing a mentor'
           ,'2017-06-25'
           ,'XUBO'
           ,3
           ,2
           ,2
           ,8)
GO


INSERT INTO [dbo].[PeerTransaction]
           ([PointsAmount]
           ,[Date]
           ,[EventDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ReceiverID]
           ,[RewarderID]
           ,[CategoryID]
           ,[ValueID])

     VALUES
           (15.00
           ,'2017-06-25'
           ,'event was based on choosing a mentor'
           ,'2017-06-25'
           ,'XUBO'
           ,3
           ,4
           ,3
           ,8)
GO


INSERT INTO [dbo].[PeerTransaction]
           ([PointsAmount]
           ,[Date]
           ,[EventDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ReceiverID]
           ,[RewarderID]
           ,[CategoryID]
           ,[ValueID])

     VALUES
           (15.00
           ,'2017-06-25'
           ,'event was held on the site'
           ,'2017-06-25'
           ,'XUBO'
           ,3
           ,4
           ,3
           ,5)
GO

INSERT INTO [dbo].[PeerTransaction]
           ([PointsAmount]
           ,[Date]
           ,[EventDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ReceiverID]
           ,[RewarderID]
           ,[CategoryID]
           ,[ValueID])

     VALUES
           (25.00
           ,'2018-08-25'
           ,'event was held on the site'
           ,'2017-06-25'
           ,'XUBO'
           ,3
           ,2
           ,3
           ,5)
GO

INSERT INTO [dbo].[PeerTransaction]
           ([PointsAmount]
           ,[Date]
           ,[EventDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ReceiverID]
           ,[RewarderID]
           ,[CategoryID]
           ,[ValueID])

     VALUES
           (25.00
           ,'2015-08-25'
           ,'event was held on the site'
           ,'2017-06-25'
           ,'XUBO'
           ,3
           ,2
           ,4
           ,5)
GO

INSERT INTO [dbo].[PeerTransaction]
           ([PointsAmount]
           ,[Date]
           ,[EventDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ReceiverID]
           ,[RewarderID]
           ,[CategoryID]
           ,[ValueID])

     VALUES
           (25.00
           ,'2015-12-25'
           ,'event was held on the site'
           ,'2017-06-25'
           ,'XUBO'
           ,3
           ,4
           ,4
           ,5)
GO

INSERT INTO [dbo].[PeerTransaction]
           ([PointsAmount]
           ,[Date]
           ,[EventDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ReceiverID]
           ,[RewarderID]
           ,[CategoryID]
           ,[ValueID])

     VALUES
           (25.00
           ,'2016-12-25'
           ,'event was held on the site'
           ,'2017-06-25'
           ,'XUBO'
           ,3
           ,4
           ,5
           ,5)
GO

INSERT INTO [dbo].[PeerTransaction]
           ([PointsAmount]
           ,[Date]
           ,[EventDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ReceiverID]
           ,[RewarderID]
           ,[CategoryID]
           ,[ValueID])

     VALUES
           (25.00
           ,'2017-12-28'
           ,'event was held on the site'
           ,'2017-06-25'
           ,'XUBO'
           ,3
           ,4
           ,5
           ,5)
GO

INSERT INTO [dbo].[PeerTransaction]
           ([PointsAmount]
           ,[Date]
           ,[EventDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ReceiverID]
           ,[RewarderID]
           ,[CategoryID]
           ,[ValueID])

     VALUES
           (25.00
           ,'2016-05-28'
           ,'event was held on the site'
           ,'2017-06-25'
           ,'XUBO'
           ,2
           ,4
           ,5
           ,5)
GO

INSERT INTO [dbo].[PeerTransaction]
           ([PointsAmount]
           ,[Date]
           ,[EventDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ReceiverID]
           ,[RewarderID]
           ,[CategoryID]
           ,[ValueID])

     VALUES
           (25.00
           ,'2016-10-15'
           ,'event was held on the site'
           ,'2017-06-25'
           ,'XUBO'
           ,3
           ,4
           ,5
           ,9)
GO

INSERT INTO [dbo].[PeerTransaction]
           ([PointsAmount]
           ,[Date]
           ,[EventDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ReceiverID]
           ,[RewarderID]
           ,[CategoryID]
           ,[ValueID])

     VALUES
           (10.00
           ,'2016-11-11'
           ,'event was held on the site'
           ,'2017-06-25'
           ,'Tatyana'
           ,3
           ,4
           ,5
           ,9)
GO

INSERT INTO [dbo].[PeerTransaction]
           ([PointsAmount]
           ,[Date]
           ,[EventDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ReceiverID]
           ,[RewarderID]
           ,[CategoryID]
           ,[ValueID])

     VALUES
           (15.00
           ,'2016-11-11'
           ,'event was held on the site'
           ,'2016-11-11'
           ,'Tatyana'
           ,2
           ,4
           ,5
           ,9)
GO
INSERT INTO [dbo].[PeerTransaction]
           ([PointsAmount]
           ,[Date]
           ,[EventDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ReceiverID]
           ,[RewarderID]
           ,[CategoryID]
           ,[ValueID])

     VALUES
           (10.00
           ,'2015-10-11'
           ,'event was held on the site'
           ,'2016-11-11'
           ,'Tatyana'
           ,2
           ,3
           ,5
           ,4)
GO
INSERT INTO [dbo].[PeerTransaction]
           ([PointsAmount]
           ,[Date]
           ,[EventDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ReceiverID]
           ,[RewarderID]
           ,[CategoryID]
           ,[ValueID])

     VALUES
           (10.00
           ,'2015-10-11'
           ,'event was held on the site'
           ,'2016-11-11'
           ,'Carol'
           ,4
           ,3
           ,5
           ,4)
GO

INSERT INTO [dbo].[PeerTransaction]
           ([PointsAmount]
           ,[Date]
           ,[EventDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ReceiverID]
           ,[RewarderID]
           ,[CategoryID]
           ,[ValueID])

     VALUES
           (25.00
           ,'2015-10-11'
           ,'event was held on the site'
           ,'2016-11-11'
           ,'Carol'
           ,4
           ,3
           ,5
           ,9)
GO

INSERT INTO [dbo].[PeerTransaction]
           ([PointsAmount]
           ,[Date]
           ,[EventDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ReceiverID]
           ,[RewarderID]
           ,[CategoryID]
           ,[ValueID])

     VALUES
           (25.00
           ,'2016-10-10'
           ,'event was held on the site'
           ,'2016-11-11'
           ,'Carol'
           ,4
           ,3
           ,5
           ,4)
GO

INSERT INTO [dbo].[PeerTransaction]
           ([PointsAmount]
           ,[Date]
           ,[EventDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ReceiverID]
           ,[RewarderID]
           ,[CategoryID]
           ,[ValueID])

     VALUES
           (15.00
           ,'2016-10-10'
           ,'event was held on the site'
           ,'2017-09-11'
           ,'Carol'
           ,2
           ,3
           ,5
           ,4)
GO

INSERT INTO [dbo].[PeerTransaction]
           ([PointsAmount]
           ,[Date]
           ,[EventDescription]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ReceiverID]
           ,[RewarderID]
           ,[CategoryID]
           ,[ValueID])

     VALUES
           (15.00
           ,'2017-09-10'
           ,'event was held on the site'
           ,'2017-09-11'
           ,'Tatyana'
           ,2
           ,4
           ,5
           ,4)
GO

INSERT INTO [dbo].[PeerTransaction]
([PointsAmount]
,[Date]
,[EventDescription]
,[LastUpdated]
,[LastUpdatedBy]
,[ReceiverID]
,[RewarderID]
,[CategoryID]
,[ValueID])
VALUES
(10.00
,'2017-04-25'
,'event was based on leadership development'
,'2017-06-25'
,'Jorge'
,5
,7
,4
,7)
GO

INSERT INTO [dbo].[PeerTransaction]
([PointsAmount]
,[Date]
,[EventDescription]
,[LastUpdated]
,[LastUpdatedBy]
,[ReceiverID]
,[RewarderID]
,[CategoryID]
,[ValueID])
VALUES
(10.00
,'2018-03-25'
,'mentorship'
,'2018-06-25'
,'Hila'
,7
,5
,3
,8)
GO

INSERT INTO [dbo].[PeerTransaction]
([PointsAmount]
,[Date]
,[EventDescription]
,[LastUpdated]
,[LastUpdatedBy]
,[ReceiverID]
,[RewarderID]
,[CategoryID]
,[ValueID])
VALUES
(10.00
,'2017-12-30'
,'mentorship'
,'2018-12-30'
,'Hila'
,7
,6
,3
,8)
GO

INSERT INTO [dbo].[PeerTransaction]
([PointsAmount]
,[Date]
,[EventDescription]
,[LastUpdated]
,[LastUpdatedBy]
,[ReceiverID]
,[RewarderID]
,[CategoryID]
,[ValueID])
VALUES
(15.00
,'2017-12-30'
,'event'
,'2018-12-30'
,'Pratic'
,5
,6
,5
,5)
GO

INSERT INTO [dbo].[PeerTransaction]
([PointsAmount]
,[Date]
,[EventDescription]
,[LastUpdated]
,[LastUpdatedBy]
,[ReceiverID]
,[RewarderID]
,[CategoryID]
,[ValueID])
VALUES
(15.00
,'2017-04-25'
,'event was based on leadership development'
,'2017-06-25'
,'Pratic'
,5
,6
,4
,7)
GO

INSERT INTO [dbo].[RewardProvider]
           ([RewardProviderName]
           ,[PhoneNumber]
           ,[Email]
           ,[Username]
           ,[Password]
           ,[Balance]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ProfilePicture])
    VALUES
           (
           'Local Roots'
           ,'7035678970'
           ,'root@gmail.com'
		   ,'rooty'
		   ,'J3Qkun24N4PsueNLq+ynBwgblehvRA=='
           ,25
           ,'2018-05-15'
           ,'Bob'
		   ,null)
GO
USE [FinalProject]
GO
INSERT INTO [dbo].[RewardProvider]
           ([RewardProviderName]
           ,[PhoneNumber]
           ,[Email]
           ,[Username]
           ,[Password]
           ,[Balance]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[ProfilePicture])
     VALUES
           (
           'Billy Jacks'
           ,'7035678970'
           ,'billy@gmail.com'
		   ,'Billy'
		   ,'mPb9MiMOW5xxx1rSwFT9idsaOVzl+fM='
           ,25
           ,'2018-05-15'
           ,'Bob'
		   ,null)
GO





INSERT INTO [dbo].[Team]
           ([CreatorID]
           ,[TeamName]
           ,[TeamDescription]
           ,[StartDate]
           ,[EndDate]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[Status]
           )
     VALUES
           (3
           ,'Team1'
           ,'group is formed to do community service'
           ,'2018-02-12'
           ,'2018-05-12'
           ,'2018-05-12'
           ,'Tatyana'
           ,1
           )
GO

INSERT INTO [dbo].[Team]
           ([CreatorID]
           ,[TeamName]
           ,[TeamDescription]
           ,[StartDate]
           ,[EndDate]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[Status]
           )
     VALUES
           (5
           ,'Team2'
           ,'group is formed to do community service'
           ,'2018-03-12'
           ,'2018-05-12'
           ,'2018-05-12'
           ,'Hila'
           ,1
           )
GO

GO









INSERT INTO [dbo].[GiftCard]
           ([RewardProviderID]
           ,[Value]
           ,[Description]
           ,[DatePosted]
           ,[Status]
           ,[DateRemoved]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[VoucherNumber]
           ,[ImageGC]
           ,[BusinessEntityID])
     VALUES
           (1,
           25
           , 'Great value for a great cause'
           ,'2018-04-09'
           ,'Active'
           ,null
           ,'2018-04-09'
           ,'Tanya'
           ,null
           ,'ss'
           ,2 )
GO


INSERT INTO [dbo].[GiftCard]
           ([RewardProviderID]
           ,[Value]
           ,[Description]
           ,[DatePosted]
           ,[Status]
           ,[DateRemoved]
           ,[LastUpdated]
           ,[LastUpdatedBy]
           ,[VoucherNumber]
           ,[ImageGC]
           ,[BusinessEntityID])
     VALUES
           (2,
           25
           , 'Great deals'
           ,'2018-04-09'
           ,'active'
           ,null
           ,'2018-04-09'
           ,'Tanya'
           ,null
           ,'ss'
           ,3 )
GO

INSERT INTO [dbo].[RewardProviderPool]
           ([BusinessEntityID]
           ,[RewardProviderID]
           ,[Status]
           ,[LastUpdated]
           ,[LastUpdatedBy])
     VALUES
           (2
           ,2
           ,'active'
           ,'2018-04-10'
           ,'tati')
GO


