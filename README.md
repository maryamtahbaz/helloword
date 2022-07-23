--
-- PostgreSQL database dump
--

-- Dumped from database version 12.9 (Ubuntu 12.9-2.pgdg20.04+1)
-- Dumped by pg_dump version 12.9 (Ubuntu 12.9-2.pgdg20.04+1)

SET statement_timeout = 0;
SET lock_timeout = 0;
SET idle_in_transaction_session_timeout = 0;
SET client_encoding = 'UTF8';
SET standard_conforming_strings = on;
SELECT pg_catalog.set_config('search_path', '', false);
SET check_function_bodies = false;
SET xmloption = content;
SET client_min_messages = warning;
SET row_security = off;

DROP DATABASE universe;
--
-- Name: universe; Type: DATABASE; Schema: -; Owner: freecodecamp
--

CREATE DATABASE universe WITH TEMPLATE = template0 ENCODING = 'UTF8' LC_COLLATE = 'C.UTF-8' LC_CTYPE = 'C.UTF-8';


ALTER DATABASE universe OWNER TO freecodecamp;

\connect universe

SET statement_timeout = 0;
SET lock_timeout = 0;
SET idle_in_transaction_session_timeout = 0;
SET client_encoding = 'UTF8';
SET standard_conforming_strings = on;
SELECT pg_catalog.set_config('search_path', '', false);
SET check_function_bodies = false;
SET xmloption = content;
SET client_min_messages = warning;
SET row_security = off;

SET default_tablespace = '';

SET default_table_access_method = heap;

--
-- Name: galaxy; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.galaxy (
    galaxy_id integer NOT NULL,
    name character varying(50),
    star_id integer,
    name2 character varying(50) NOT NULL,
    name3 character varying(50)
);


ALTER TABLE public.galaxy OWNER TO freecodecamp;

--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.galaxy_galaxy_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.galaxy_galaxy_id_seq OWNER TO freecodecamp;

--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.galaxy_galaxy_id_seq OWNED BY public.galaxy.galaxy_id;


--
-- Name: moon; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.moon (
    moon_id integer NOT NULL,
    name character varying(50),
    name2 character varying(50) NOT NULL,
    name4 character varying(50),
    name3 character varying(50)
);


ALTER TABLE public.moon OWNER TO freecodecamp;

--
-- Name: moon_moon_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.moon_moon_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.moon_moon_id_seq OWNER TO freecodecamp;

--
-- Name: moon_moon_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.moon_moon_id_seq OWNED BY public.moon.moon_id;


--
-- Name: planet; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.planet (
    planet_id integer NOT NULL,
    name character varying(50),
    name2 character varying(50) NOT NULL,
    name3 character varying(50),
    name4 character varying(50)
);


ALTER TABLE public.planet OWNER TO freecodecamp;

--
-- Name: planet_planet_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.planet_planet_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.planet_planet_id_seq OWNER TO freecodecamp;

--
-- Name: planet_planet_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.planet_planet_id_seq OWNED BY public.planet.planet_id;


--
-- Name: star; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.star (
    star_id integer NOT NULL,
    name character varying(50),
    int1 integer,
    int2 integer,
    num numeric(4,2),
    b1 integer,
    b2 boolean,
    t1 text,
    b3 boolean,
    galaxy_id integer,
    name2 character varying(50) NOT NULL
);


ALTER TABLE public.star OWNER TO freecodecamp;

--
-- Name: star2; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.star2 (
    star2_id integer NOT NULL,
    name character varying(50) NOT NULL,
    name2 character varying(50)
);


ALTER TABLE public.star2 OWNER TO freecodecamp;

--
-- Name: star2_star2_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.star2_star2_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.star2_star2_id_seq OWNER TO freecodecamp;

--
-- Name: star2_star2_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.star2_star2_id_seq OWNED BY public.star2.star2_id;


--
-- Name: star_star_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.star_star_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.star_star_id_seq OWNER TO freecodecamp;

--
-- Name: star_star_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.star_star_id_seq OWNED BY public.star.star_id;


--
-- Name: galaxy galaxy_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy ALTER COLUMN galaxy_id SET DEFAULT nextval('public.galaxy_galaxy_id_seq'::regclass);


--
-- Name: moon moon_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon ALTER COLUMN moon_id SET DEFAULT nextval('public.moon_moon_id_seq'::regclass);


--
-- Name: planet planet_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet ALTER COLUMN planet_id SET DEFAULT nextval('public.planet_planet_id_seq'::regclass);


--
-- Name: star star_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star ALTER COLUMN star_id SET DEFAULT nextval('public.star_star_id_seq'::regclass);


--
-- Name: star2 star2_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star2 ALTER COLUMN star2_id SET DEFAULT nextval('public.star2_star2_id_seq'::regclass);


--
-- Data for Name: galaxy; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.galaxy VALUES (1, 'D', NULL, 'G', NULL);
INSERT INTO public.galaxy VALUES (2, 'R', NULL, 'F', NULL);
INSERT INTO public.galaxy VALUES (3, 'W', NULL, 'E', NULL);
INSERT INTO public.galaxy VALUES (4, 'Q', NULL, 'A', NULL);
INSERT INTO public.galaxy VALUES (5, 'Y', NULL, 'S', NULL);
INSERT INTO public.galaxy VALUES (6, 'T', NULL, 'L', NULL);


--
-- Data for Name: moon; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.moon VALUES (1, 'A', '', 'D', 'C');
INSERT INTO public.moon VALUES (2, 'E', 'F', 'H', 'G');
INSERT INTO public.moon VALUES (3, 'I', 'J', 'L', 'K');
INSERT INTO public.moon VALUES (4, 'E', 'S', 'H', 'G');
INSERT INTO public.moon VALUES (5, 'I', 'D', 'L', 'K');
INSERT INTO public.moon VALUES (6, 'E', '2S', 'H', 'G');
INSERT INTO public.moon VALUES (7, 'I', '1D', 'L', 'K');
INSERT INTO public.moon VALUES (8, 'E', '3S', 'H', 'G');
INSERT INTO public.moon VALUES (9, 'I', '2D', 'L', 'K');
INSERT INTO public.moon VALUES (10, 'E', '4S', 'H', 'G');
INSERT INTO public.moon VALUES (11, 'I', '3D', 'L', 'K');
INSERT INTO public.moon VALUES (12, '1', '2', '4', '3');
INSERT INTO public.moon VALUES (13, '1', '22', '4', '3');
INSERT INTO public.moon VALUES (14, '1', '252', '4', '3');
INSERT INTO public.moon VALUES (15, '1', '26', '4', '3');
INSERT INTO public.moon VALUES (16, '1', '36', '4', '3');
INSERT INTO public.moon VALUES (17, '1', '66', '4', '3');
INSERT INTO public.moon VALUES (18, '1', '67', '4', '3');
INSERT INTO public.moon VALUES (19, '1', '667', '4', '3');
INSERT INTO public.moon VALUES (20, '1', '687', '4', '3');


--
-- Data for Name: planet; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.planet VALUES (1, 'A', '', 'C', 'D');
INSERT INTO public.planet VALUES (2, 'E', 'F', 'G', 'H');
INSERT INTO public.planet VALUES (3, 'I', 'J', 'K', 'L');
INSERT INTO public.planet VALUES (4, 'E', 'S', 'G', 'H');
INSERT INTO public.planet VALUES (5, 'I', 'D', 'K', 'L');
INSERT INTO public.planet VALUES (6, 'E', '2S', 'G', 'H');
INSERT INTO public.planet VALUES (7, 'I', '1D', 'K', 'L');
INSERT INTO public.planet VALUES (8, 'E', '3S', 'G', 'H');
INSERT INTO public.planet VALUES (9, 'I', '2D', 'K', 'L');
INSERT INTO public.planet VALUES (10, 'E', '4S', 'G', 'H');
INSERT INTO public.planet VALUES (11, 'I', '3D', 'K', 'L');
INSERT INTO public.planet VALUES (12, '1', '2', '3', '4');
INSERT INTO public.planet VALUES (13, '1', '22', '3', '4');
INSERT INTO public.planet VALUES (14, '1', '252', '3', '4');
INSERT INTO public.planet VALUES (15, '1', '26', '3', '4');
INSERT INTO public.planet VALUES (16, '1', '36', '3', '4');
INSERT INTO public.planet VALUES (17, '1', '66', '3', '4');
INSERT INTO public.planet VALUES (18, '1', '67', '3', '4');
INSERT INTO public.planet VALUES (19, '1', '667', '3', '4');
INSERT INTO public.planet VALUES (20, '1', '687', '3', '4');


--
-- Data for Name: star; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.star VALUES (1, 'D', NULL, NULL, NULL, NULL, NULL, NULL, NULL, NULL, 'G');
INSERT INTO public.star VALUES (2, 'R', NULL, NULL, NULL, NULL, NULL, NULL, NULL, NULL, 'F');
INSERT INTO public.star VALUES (3, 'W', NULL, NULL, NULL, NULL, NULL, NULL, NULL, NULL, 'E');
INSERT INTO public.star VALUES (4, 'Q', NULL, NULL, NULL, NULL, NULL, NULL, NULL, NULL, 'A');
INSERT INTO public.star VALUES (5, 'Y', NULL, NULL, NULL, NULL, NULL, NULL, NULL, NULL, 'S');
INSERT INTO public.star VALUES (6, 'T', NULL, NULL, NULL, NULL, NULL, NULL, NULL, NULL, 'L');


--
-- Data for Name: star2; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.star2 VALUES (1, 'D', 'G');
INSERT INTO public.star2 VALUES (2, 'R', 'F');
INSERT INTO public.star2 VALUES (3, 'W', 'E');
INSERT INTO public.star2 VALUES (4, 'Q', 'A');
INSERT INTO public.star2 VALUES (5, 'Y', 'S');
INSERT INTO public.star2 VALUES (6, 'T', 'L');


--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.galaxy_galaxy_id_seq', 1, false);


--
-- Name: moon_moon_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.moon_moon_id_seq', 1, false);


--
-- Name: planet_planet_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.planet_planet_id_seq', 1, false);


--
-- Name: star2_star2_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.star2_star2_id_seq', 1, false);


--
-- Name: star_star_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.star_star_id_seq', 1, false);


--
-- Name: galaxy galaxy_name2_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy
    ADD CONSTRAINT galaxy_name2_key UNIQUE (name2);


--
-- Name: galaxy galaxy_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy
    ADD CONSTRAINT galaxy_pkey PRIMARY KEY (galaxy_id);


--
-- Name: moon moon_name2_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_name2_key UNIQUE (name2);


--
-- Name: moon moon_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_pkey PRIMARY KEY (moon_id);


--
-- Name: planet planet_name2_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_name2_key UNIQUE (name2);


--
-- Name: planet planet_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_pkey PRIMARY KEY (planet_id);


--
-- Name: star2 star2_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star2
    ADD CONSTRAINT star2_name_key UNIQUE (name);


--
-- Name: star2 star2_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star2
    ADD CONSTRAINT star2_pkey PRIMARY KEY (star2_id);


--
-- Name: star star_name2_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_name2_key UNIQUE (name2);


--
-- Name: star star_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_pkey PRIMARY KEY (star_id);


--
-- Name: galaxy galaxy_star_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy
    ADD CONSTRAINT galaxy_star_id_fkey FOREIGN KEY (star_id) REFERENCES public.star(star_id);


--
-- Name: star star_galaxy_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_galaxy_id_fkey FOREIGN KEY (galaxy_id) REFERENCES public.galaxy(galaxy_id);


--
-- PostgreSQL database dump complete
--

