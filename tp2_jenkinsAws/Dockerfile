FROM nginx:alpine

# Supprime TOUTE la configuration par défaut
RUN rm -rf /etc/nginx/conf.d/*

# Copie votre application
COPY app/ /usr/share/nginx/html

# Ajoute une configuration Nginx minimale
RUN echo "server { \
    listen 81; \
    root /usr/share/nginx/html; \
    index index.html; \
    location / { try_files \$uri \$uri/ =404; } \
    }" > /etc/nginx/conf.d/default.conf

