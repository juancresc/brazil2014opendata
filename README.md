brazil2014opendata
==================

Teams, matches, places and groups in MySQL

CAREFUL: First insert groups, places, then teams and finally matches :)

Or you can copy this

```

CREATE TABLE IF NOT EXISTS `FootballMatch` (
  `id_footballMatch` int(11) NOT NULL AUTO_INCREMENT,
  `time` time NOT NULL,
  `date` date NOT NULL,
  `team1` int(11) NOT NULL,
  `team2` int(11) NOT NULL,
  `number` int(11) NOT NULL,
  `round` int(11) NOT NULL,
  `place` int(11) NOT NULL,
  PRIMARY KEY (`id_footballMatch`),
  KEY `fk_footballMarch_place` (`place`),
  KEY `fk_footballMarch_team1` (`team1`),
  KEY `fk_footballMarch_team2` (`team2`),
  KEY `fk_footballMarch_round` (`round`)
) ENGINE=InnoDB  DEFAULT CHARSET=latin1 AUTO_INCREMENT=50 ;


INSERT INTO `FootballMatch` (`id_footballMatch`, `time`, `date`, `team1`, `team2`, `number`, `round`, `place`) VALUES
(2, '21:00:00', '2014-06-12', 6, 11, 1, 1, 12),
(3, '17:00:00', '2014-06-13', 24, 7, 2, 1, 7),
(4, '20:00:00', '2014-06-13', 29, 25, 3, 1, 11),
(5, '23:00:00', '2014-06-13', 8, 3, 4, 1, 4),
(6, '17:00:00', '2014-06-14', 9, 18, 5, 1, 1),
(7, '02:00:00', '2014-06-15', 12, 22, 6, 1, 9),
(8, '20:00:00', '2014-06-14', 4, 10, 7, 1, 5),
(9, '23:00:00', '2014-06-14', 14, 21, 8, 1, 6),
(10, '17:00:00', '2014-06-15', 30, 13, 9, 1, 2),
(11, '20:00:00', '2014-06-15', 15, 19, 10, 1, 8),
(12, '23:00:00', '2014-07-15', 2, 5, 11, 1, 10),
(13, '17:00:00', '2014-07-16', 16, 27, 12, 1, 11),
(14, '20:00:00', '2014-07-16', 20, 26, 13, 1, 4),
(15, '23:00:00', '2014-07-16', 17, 32, 14, 1, 7),
(16, '17:00:00', '2014-07-17', 4, 1, 15, 1, 1),
(17, '20:00:00', '2014-07-17', 6, 24, 16, 1, 5),
(18, '23:00:00', '2014-07-17', 28, 23, 17, 1, 3),
(19, '17:00:00', '2014-07-18', 3, 25, 18, 1, 8),
(20, '23:00:00', '2014-07-18', 7, 11, 19, 1, 6),
(21, '20:00:00', '2014-07-18', 29, 8, 20, 1, 10),
(22, '17:00:00', '2014-07-19', 9, 12, 21, 1, 2),
(23, '20:00:00', '2014-07-19', 31, 14, 22, 1, 12),
(24, '23:00:00', '2014-07-19', 22, 18, 23, 1, 7),
(25, '17:00:00', '2014-07-20', 21, 10, 24, 1, 9),
(26, '20:00:00', '2014-07-20', 30, 15, 25, 1, 11),
(27, '23:00:00', '2014-07-20', 19, 13, 26, 1, 4),
(28, '17:00:00', '2014-07-21', 2, 20, 27, 1, 1),
(29, '20:00:00', '2014-07-21', 16, 17, 28, 1, 5),
(30, '23:00:00', '2014-07-21', 26, 5, 29, 1, 3),
(31, '20:00:00', '2014-07-22', 23, 1, 30, 1, 8),
(32, '23:00:00', '2014-07-22', 32, 27, 31, 1, 6),
(33, '17:00:00', '2014-07-22', 4, 28, 32, 1, 10),
(34, '17:00:00', '2014-07-23', 3, 29, 33, 1, 4),
(35, '17:00:00', '2014-07-23', 25, 8, 34, 1, 12),
(36, '21:00:00', '2014-07-23', 7, 6, 35, 1, 2),
(37, '21:00:00', '2014-07-23', 11, 24, 36, 1, 9),
(38, '17:00:00', '2014-07-24', 21, 31, 37, 1, 7),
(39, '17:00:00', '2014-07-24', 10, 14, 38, 1, 1),
(40, '21:00:00', '2014-07-24', 22, 9, 39, 1, 3),
(41, '21:00:00', '2014-07-24', 18, 12, 40, 1, 5),
(42, '17:00:00', '2014-07-25', 26, 2, 41, 1, 8),
(43, '17:00:00', '2014-07-25', 5, 20, 42, 1, 11),
(44, '21:00:00', '2014-07-25', 19, 30, 43, 1, 6),
(45, '21:00:00', '2014-07-25', 13, 15, 44, 1, 10),
(46, '17:00:00', '2014-07-26', 32, 16, 45, 1, 9),
(47, '17:00:00', '2014-07-26', 27, 17, 46, 1, 2),
(48, '21:00:00', '2014-07-26', 23, 4, 47, 1, 12),
(49, '21:00:00', '2014-07-26', 1, 28, 48, 1, 4);


CREATE TABLE IF NOT EXISTS `Place` (
  `id_place` int(11) NOT NULL AUTO_INCREMENT,
  `name` varchar(200) NOT NULL,
  PRIMARY KEY (`id_place`)
) ENGINE=InnoDB  DEFAULT CHARSET=latin1 AUTO_INCREMENT=13 ;


INSERT INTO `Place` (`id_place`, `name`) VALUES
(1, 'Belo Horizonte'),
(2, 'Brasilia'),
(3, 'Cuiaba'),
(4, 'Curitiba'),
(5, 'Fortaleza'),
(6, 'Manaus'),
(7, 'Natal'),
(8, 'Porto Alegre'),
(9, 'Recife'),
(10, 'Rio De Janeiro'),
(11, 'Salvador'),
(12, 'Sao Paulo');


CREATE TABLE IF NOT EXISTS `Result` (
  `id_result` int(11) NOT NULL AUTO_INCREMENT,
  `footballMatch` int(11) NOT NULL,
  `team1score` int(11) NOT NULL,
  `team2score` int(11) NOT NULL,
  `active` int(11) NOT NULL DEFAULT '1',
  PRIMARY KEY (`id_result`),
  KEY `fk_result_footballMatch` (`footballMatch`)
) ENGINE=InnoDB  DEFAULT CHARSET=latin1 AUTO_INCREMENT=2 ;


INSERT INTO `Result` (`id_result`, `footballMatch`, `team1score`, `team2score`, `active`) VALUES
(1, 2, 1, 4, 1);


CREATE TABLE IF NOT EXISTS `Round` (
  `id_round` int(11) NOT NULL AUTO_INCREMENT,
  `name` varchar(200) NOT NULL,
  `enabled` int(11) NOT NULL DEFAULT '0',
  PRIMARY KEY (`id_round`)
) ENGINE=InnoDB  DEFAULT CHARSET=latin1 AUTO_INCREMENT=7 ;


INSERT INTO `Round` (`id_round`, `name`, `enabled`) VALUES
(1, 'Etapa de Grupos', 1),
(2, 'Ronda de 16', 0),
(3, 'Cuartos de Final', 0),
(4, 'Semifinal', 0),
(5, 'Tercer y cuarto puesto', 0),
(6, 'Final', 0);


CREATE TABLE IF NOT EXISTS `Team` (
  `id_team` int(11) NOT NULL AUTO_INCREMENT,
  `name` varchar(200) NOT NULL,
  `teamGroup` int(11) NOT NULL,
  PRIMARY KEY (`id_team`),
  KEY `fk_team_teamGroup` (`teamGroup`)
) ENGINE=InnoDB  DEFAULT CHARSET=latin1 AUTO_INCREMENT=34 ;


INSERT INTO `Team` (`id_team`, `name`, `teamGroup`) VALUES
(1, 'Algeria', 8),
(2, 'Argentina', 6),
(3, 'Australia', 2),
(4, 'Belgium', 8),
(5, 'Bosnia-Herzegovina', 6),
(6, 'Brazil', 1),
(7, 'Cameroon', 1),
(8, 'Chile', 2),
(9, 'Colombia', 3),
(10, 'Costa Rica', 4),
(11, 'Croatia', 1),
(12, 'Côte d''Ivoire', 3),
(13, 'Ecuador', 5),
(14, 'England', 4),
(15, 'France', 5),
(16, 'Germany', 7),
(17, 'Ghana', 7),
(18, 'Greece', 3),
(19, 'Honduras', 5),
(20, 'Iran', 6),
(21, 'Italy', 4),
(22, 'Japan', 3),
(23, 'Korea Republic', 8),
(24, 'Mexico', 1),
(25, 'Netherlands', 2),
(26, 'Nigeria', 6),
(27, 'Portugal', 7),
(28, 'Russia', 8),
(29, 'Spain', 2),
(30, 'Switzerland', 5),
(31, 'Uruguay', 4),
(32, 'USA', 7);


CREATE TABLE IF NOT EXISTS `TeamGroup` (
  `id_teamGroup` int(11) NOT NULL AUTO_INCREMENT,
  `name` varchar(200) NOT NULL,
  PRIMARY KEY (`id_teamGroup`)
) ENGINE=InnoDB  DEFAULT CHARSET=latin1 AUTO_INCREMENT=9 ;


INSERT INTO `TeamGroup` (`id_teamGroup`, `name`) VALUES
(1, 'A'),
(2, 'B'),
(3, 'C'),
(4, 'D'),
(5, 'E'),
(6, 'F'),
(7, 'G'),
(8, 'H');


ALTER TABLE `FootballMatch`
  ADD CONSTRAINT `fk_footballMarch_place` FOREIGN KEY (`place`) REFERENCES `Place` (`id_place`),
  ADD CONSTRAINT `fk_footballMarch_round` FOREIGN KEY (`round`) REFERENCES `Round` (`id_round`),
  ADD CONSTRAINT `fk_footballMarch_team1` FOREIGN KEY (`team1`) REFERENCES `Team` (`id_team`),
  ADD CONSTRAINT `fk_footballMarch_team2` FOREIGN KEY (`team2`) REFERENCES `Team` (`id_team`);

ALTER TABLE `Result`
  ADD CONSTRAINT `fk_result_footballMatch` FOREIGN KEY (`footballMatch`) REFERENCES `FootballMatch` (`id_footballMatch`);

ALTER TABLE `Team`
  ADD CONSTRAINT `fk_team_teamGroup` FOREIGN KEY (`teamGroup`) REFERENCES `TeamGroup` (`id_teamGroup`);

```
