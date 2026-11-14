FROM ghcr.io/dimap/yapanel-web:latest
# Device ID Станции Лайт вида LR... содержит не только hex-символы: расширяем проверку идентификатора в панели
RUN sed -i 's/\[A-Fa-f0-9\]{32}/[A-Za-z0-9]{32}/' /app/model_colors.py \
 && grep -q 'A-Za-z0-9\]{32}' /app/model_colors.py
ENV ADB_SERIAL="192.168.1.20"
ENV PANEL_HOST="0.0.0.0"
ENV PANEL_PORT="8765"
ENV PANEL_HTTPS_PORT="0"
