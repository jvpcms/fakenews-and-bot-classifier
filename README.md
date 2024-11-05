# Reddit-API-ORM
Esta aplicação em Python foi desenvolvida com o objetivo de simplificar e abstrair a comunicação com a API do Reddit, proporcionando uma interface organizada e orientada a objetos para interações com os dados da plataforma. Inspirada por um modelo de ORM (Object-Relational Mapping), a aplicação encapsula as requisições HTTP, permitindo que operações na API do Reddit sejam realizadas de maneira intuitiva, utilizando classes e objetos para representar posts, perfis de usuários, subreddits e outras entidades relevantes.

O desenvolvimento dessa aplicação é motivado pela necessidade de extrair dados de publicações de notícias e construir conjuntos de dados consistentes sobre notícias falsas e verdadeiras, para aplicações em inteligência artificial, como treinamento de modelos de classificação. Além disso, a aplicação permite a coleta de dados sobre perfis de usuários, possibilitando a análise e a classificação de contas como bots ou não-bots com base em suas atividades e características comportamentais.

## Setup

## Basic Use
```python
    client = RedditClient()

    # buscar publicações
    posts = client.posts().search("Latest News").execute()

    # usuários e subreddits
    for post in posts:
        user = client.users().about(post.author).execute()
        subreddit = client.subreddits().about(post.subreddit).execute()
```
