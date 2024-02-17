# Host_py
Servidor Compartilhado Python para Aplicações Web
Este repositório contém os arquivos necessários para configurar um servidor compartilhado Python, projetado para hospedar e executar aplicações web em Python. Este servidor é baseado em contêineres Docker, oferecendo um ambiente isolado e escalável para desenvolvedores e usuários finais.

## Funcionalidades Principais:
- Isolamento de Ambiente: Cada aplicação é executada em um contêiner Docker isolado, garantindo segurança e consistência no ambiente de execução.

- Facilidade de Implantação: As aplicações Python podem ser implantadas facilmente utilizando contêineres Docker, permitindo uma implantação suave e consistente.

- Flexibilidade de Configuração: O servidor é altamente configurável, permitindo ajustes de recursos, configurações de rede e personalização do ambiente de execução.

### Como Utilizar: 
Instalação do Docker: Certifique-se de ter o Docker instalado em sua máquina. Você pode encontrar instruções de instalação no site oficial do Docker.

Clonar este Repositório: Clone este repositório para o seu ambiente local:

git clone [https://github.com/](https://github.com/euforo/Host_py/e)https://github.com/euforo/Host_py.git

Construção da Imagem Docker: Construa a imagem Docker a partir do Dockerfile fornecido:
docker build -t python-server .

Execução do Servidor: Execute o servidor em um contêiner Docker:
docker run -d -p 8000:8000 --name python-server-container python-server


Obs: Nesse momento o projeto está em desenvolvimento.
