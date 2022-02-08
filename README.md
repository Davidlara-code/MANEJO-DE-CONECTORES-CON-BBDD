# MANEJO-DE-CONECTORES-CON-BBDD


Para usar esta aplicacion es necesario crear estas tablas en una base de datos llamada "bbdd" no soy el mas original para los nombres, pero FUNCIONAN.


CREATE TABLE `coches` (
  `id` INT NOT NULL AUTO_INCREMENT,
  `matricula` VARCHAR(45) NULL,
  `marca` VARCHAR(45) NULL,
  `modelo` VARCHAR(45) NULL,
  `color` VARCHAR(45) NULL,
  PRIMARY KEY (`id`));
  
  
CREATE TABLE `personas` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `nombre` varchar(45) DEFAULT NULL,
  `edad` int(3) DEFAULT NULL,
  `peso` int(3) DEFAULT NULL,
  `id_coches` int  NULL ,
   foreign key (id_coches) references coches(id),
  PRIMARY KEY (`id`)
);
