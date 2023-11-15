# animated-octo-palm-tree
Рекомендательная система фильмов
Будем использовать набор данных https://gist.github.com/tiangechen/b68782efa49a16edaf07dc2cdaa855ea1
https://gist.github.com/marcelcaraciolo/3351277
96|Коля (1996)|3
186|L.A. Confidential (1997)|3
22|Тяжеловесы (1994)|1
244|Легенды осени (1994)|2
166|Джеки Браун (1997)|1
298|Доктор Стрейнджлав или: Как я научился перестать беспокоиться и полюбил бомбу (1963)|4
115|Охота за Красным Октябрем (1990)|2
253|Книга джунглей (1994)|5
305|Смазка (1978)|3
movie_names=pd.read_csv('/content/gdrive/My Drive/COLAB_Andemir/movies.csv')
movie_names.head() 
      title        genres
1 Молодежь в бунте	Юмор	
2 Вы встретите Высокого Темноволосого Незнакомца	Юмор	
3 Когда в Риме	Юмор	
4 Что происходит в Вегасе	Юмор
movie_data = pd.merge(ratings_data, movie_names, on = 'movieid')
movie_data.head()
выведем среднее значение
movie_data.groupby('title')['rating'].mean().head()
movie_data.groupby('title')['raiting'].mean().sort_values(ascending=False).head
movie_data.groupby('title')['rating'].count().sort_values(ascending=False).head()
ratings_mean_count = pd.DataFrame(movie_data_groupby('title')['ratings'].mean())
ratings_mean_count['rating_counts'] = pd.DataFrame(movie_data.groupby('title")['rating'].count())
ratings_mean_count.head()
