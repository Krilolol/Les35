# Les35

Monitoring
1. Розгортання інфраструктури:
- За допомогою terraform створив 2 сервери: app та monitoring
![1](https://github.com/user-attachments/assets/ef9eb65e-9678-4708-b8df-f35a93083229)


2. Налаштування моніторинг-серверу:
- На сервер моніторингу за допомогою ansible-playbook monitoring.yml встановив Docker, Docker-compose, node_exporter, скопіював локальні конфіги для Grafana, Loki та Prometheus і запустив їх
![2](https://github.com/user-attachments/assets/9eef9943-a35a-48dd-8728-b12e6c36789a)
![3](https://github.com/user-attachments/assets/9c6aa406-2119-4288-b52d-6ccf74c1e09b)
![4](https://github.com/user-attachments/assets/75d56c6b-8238-44df-a222-7a1c321f5d51)
![5](https://github.com/user-attachments/assets/a41ebb6c-d2c5-4043-83d2-c6f6280e7094)

3. Налаштування app-серверу:
- На app сервер за допомогою ansible-playbook app.yml встановив Docker, Docker-compose, node_exporter, скопіював конфіг для Promtail та запустив його докер образ
![6](https://github.com/user-attachments/assets/85125367-b6d7-48db-9f6b-4fcaee40575b)
![7](https://github.com/user-attachments/assets/4bf9544f-e881-4175-a456-6199f8653d70)
![8](https://github.com/user-attachments/assets/6d478d99-c262-4784-bf70-9662cfb87b42)

4. Налаштувати Grafana:
- Додав 2 data source: Prometheus та Loki
- Імпортував дашборди Node Exporter, Nginx Dashboard, Loki Logs Explorer
- У результаті маю налаштовані метрики, що відображаються в дашборді, логи з Nginx серверу
![9](https://github.com/user-attachments/assets/39ef24ad-f5e7-4ed6-9442-ae50463b1a47)
![10](https://github.com/user-attachments/assets/109b8e1e-5f89-4b94-85e6-c0b99c3a7399)
![11](https://github.com/user-attachments/assets/e429f748-b763-4dea-a1f6-59ab94562901)
![12](https://github.com/user-attachments/assets/abe7e61d-68a4-41c8-92cb-d0c0ff94eec6)
