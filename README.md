# 🎓 Papa Mike CRM - Sistema de Gestão Escolar & Automação Comercial

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white)

O **Papa Mike CRM** é um ecossistema educacional personalizado, desenvolvido para otimizar o Pipeline de Vendas e garantir a integração fluida entre os setores Comercial e de Coordenação Pedagógica. Construído com uma arquitetura baseada em microserviços, ele atua como o motor central de matrículas da instituição, garantindo que nenhum potencial aluno seja perdido por falhas de processo.

Desenvolvido para eliminar a perda de leads, automatizar cálculos financeiros complexos e trazer a operação escolar para a era da comunicação instantânea.

---

## 🚀 Principais Funcionalidades (O Cérebro do Sistema)

### 1. 🔄 Pipeline Integrado & Fila Pedagógica
Diferente de CRMs genéricos, o Papa Mike CRM entende o fluxo real de uma escola. Quando um novo lead chega (Recepção), ele não vai direto para vendas. O sistema possui um **Check-in Pedagógico**, que encaminha o aluno para uma "Fila de Espera" exclusiva para triagem da coordenação antes da liberação comercial. Nada avança sem o aval pedagógico.

### 2. 💰 Motor Financeiro Anti-Falhas
O sistema possui regras de negócio estritas (*Hardcoded Business Rules*) para proteger o caixa da escola. A lógica de descontos automatizada trava a aplicação de abatimentos na matrícula ou material didático. Qualquer percentual de desconto incide exclusivamente sobre a mensalidade, eliminando o risco de erros operacionais no fechamento de contratos.

### 3. 📱 UX Inovadora: Modo Apresentação (180º)
O layout foi projetado com filosofia **Mobile-First**, utilizando unidades `100dvh` para garantir a usabilidade perfeita em tablets. Para o momento do "fechamento", desenvolvemos o **Modo Apresentação**: com um toque, a interface rotaciona 180 graus e entra em alto contraste (Blackout), permitindo que o consultor apresente a proposta financeira ao pai/responsável do outro lado da mesa, sem precisar girar o dispositivo fisicamente.

### 4. 🤖 Automação de Comunicação (Evolution API)
Integração nativa com a **Evolution API** para automação de WhatsApp. O sistema não espera a equipe comercial agir passivamente; ele monitora o status dos leads e a agenda corporativa para disparar notificações instantâneas e lembretes de visitas automáticos, reduzindo o *churn* e o tempo de resposta.

### 5. 🐳 Infraestrutura Resiliente & Portável
Toda a arquitetura é containerizada. A aplicação Node.js, o banco de dados PostgreSQL e a API do WhatsApp rodam em containers isolados via **Docker**. Isso garante que o deploy em qualquer servidor VPS Linux seja feito em minutos (`docker compose up`), blindando o sistema contra conflitos de dependência do sistema operacional.

---

## 🛠️ Arquitetura e Tecnologias

* **Frontend:** React.js + Vite
* **Backend:** Node.js + Express
* **Banco de Dados:** PostgreSQL
* **Integração / Mensageria:** Evolution API (WhatsApp)
* **Estilização:** Tailwind CSS + Framer Motion (Animações)
* **Infraestrutura / DevOps:** Docker, Docker Compose, Linux (Ubuntu Server)

---

## ⚙️ Como rodar o projeto localmente

### 1. Clone o repositório
```bash
git clone [https://github.com/SEU_USUARIO/papamike-crm.git](https://github.com/SEU_USUARIO/papamike-crm.git)
cd papamike-crm
```

### 2. Configure as Variáveis de Ambiente
Crie um arquivo `.env` na raiz do projeto baseado no `.env.example`:

```env
PORT=3000
DATABASE_URL="postgresql://usuario:senha@db:5432/papamike"
EVOLUTION_API_URL="http://evolution_api:8080"
EVOLUTION_API_KEY="sua_chave_secreta"
```

### 3. Suba a Infraestrutura com Docker
Certifique-se de ter o Docker e o Docker Compose instalados na sua máquina.

```bash
# Constrói as imagens e sobe os containers em background
docker compose up -d --build
```

### 4. Acesso
* **Frontend:** `http://localhost:5173`
* **Backend API:** `http://localhost:3000`

---

## 👨‍💻 Autor

Desenvolvido com ☕ e foco em performance por **Kauã**.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/kaua-alves-silva/)
