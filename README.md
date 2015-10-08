# EADMiniProject
AZD Engines Company 

//Database

CREATE TABLE EngineModel(
	ModelID int primary key not null,
	EngineName varchar(50) not null,
	EngineDescription varchar(500),
	FuelType varchar(50) not null,
	Cylinders int not null,
	CubicCapacity float not null,
	Quantity int,
	Cost real not null,
	SellingPrice real,
	Discount real,
	AuthorizePerson varchar(50),
	EngineImage varchar(200)
);

CREATE TABLE EngineType(
	EngineID int AUTO_INCREMENT primary key,
	ModelID int,
        foreign key(ModelID) references EngineModel(ModelID)
);
CREATE TABLE EngineParts(
	PartID int primary key not null,
	PartName varchar(50) not null,
	PartDescription varchar(500),
	Cost real not null,
	Quantity int,
        EngineImage varchar(200)
);

insert into EngineModel(ModelID,EngineName,FuelType,Cylinders,CubicCapacity,Cost) values(1,"A","diesel",2,30,10000)
