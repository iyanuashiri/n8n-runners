FROM n8nio/runners:1.121.0
USER root
RUN cd /opt/runners/task-runner-javascript && pnpm add moment uuid adm-zip
RUN cd /opt/runners/task-runner-python && uv pip install numpy pandas pydantic requests
COPY n8n-task-runners.json /etc/n8n-task-runners.json
ENV N8N_RUNNERS_CONFIG_FILE=/etc/n8n-task-runners.json
USER runner

