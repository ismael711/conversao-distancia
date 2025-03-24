# Conversão de Distância - Aplicação Web

## Sobre o Projeto
Esta é uma aplicação web desenvolvida em Python que realiza a conversão de unidades de distância. O foco principal do projeto está na sua estrutura DevOps, garantindo escalabilidade, automação e implantação contínua.

## Tecnologias Utilizadas
- **Linguagem:** Python
- **Containerização:** Docker
- **Orquestração:** Kubernetes (GKE)
- **CI/CD:** GitHub Actions
- **Infraestrutura como Código (IaC):** Terraform (em breve)

## Estrutura DevOps

### Docker
A aplicação é empacotada em um contêiner Docker disponível no Docker Hub:

```sh
 docker pull ismael07111/conversao-distancia
```

### Kubernetes (GKE)
A aplicação roda em um cluster Kubernetes no **Google Kubernetes Engine (GKE)**, utilizando um serviço do tipo **LoadBalancer** para garantir alta disponibilidade e escalabilidade.

#### Deploy no Kubernetes:
```sh
kubectl apply -f k8s/deployment.yaml
```

### CI/CD com GitHub Actions
O pipeline de CI/CD realiza as seguintes etapas:
1. **Build & Test:** Valida a aplicação e executa testes automatizados.
2. **Docker Build & Push:** Criação da imagem Docker e publicação no Docker Hub.
3. **Deploy no GKE:** Aplicação da configuração no cluster Kubernetes.

## Como Executar Localmente

1. Clone o repositório:
   ```sh
   git clone https://github.com/ismael711/conversao-distancia.git
   cd conversao-distancia
   ```
2. Execute com Docker:
   ```sh
   docker run -p 5000:5000 ismael07111/conversao-distancia
   ```
3. Acesse a aplicação no navegador: `http://localhost:5000`

## Melhorias Futuras
- Implementação do Terraform para gerenciar a infraestrutura.
- Monitoramento com Prometheus e Grafana.
- Expansão das unidades de conversão suportadas.

## Contribuição
Contribuições são bem-vindas! Sinta-se à vontade para abrir issues e pull requests.

---
Criado por [Ismael](https://github.com/ismael711). 🚀
