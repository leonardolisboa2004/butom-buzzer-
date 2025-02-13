

---

# 📢 Projeto: Buzzer com Raspberry Pi Pico  

Este projeto implementa um **buzzer** acionado por um **botão** usando o **Raspberry Pi Pico**. O código utiliza **PWM (Pulse Width Modulation)** para controlar a frequência do som gerado pelo buzzer.  

## 🛠 Requisitos  

- **Raspberry Pi Pico**  
- **Buzzer ativo ou passivo**  
- **Botão push-button**  
- **Resistor de pull-up** (se necessário)  
- **Placa de ensaio e fios jumper**  
- **VS Code** com a extensão do **Raspberry Pi Pico** instalada  

## 🖥 Configuração do Ambiente no VS Code  

### 1️⃣ Instalar a Extensão do Raspberry Pi Pico  
1. Abra o **VS Code**.  
2. Vá até a aba de **Extensões** (`Ctrl+Shift+X`).  
3. Pesquise por **"Raspberry Pi Pico SDK"**.  
4. Instale a extensão **"Raspberry Pi Pico"** oficial.  

### 2️⃣ Configurar o Projeto no VS Code  
1. No **VS Code**, abra a pasta do projeto.  
2. Pressione `F1` e pesquise **"Pico: Configure Project"**, selecione e aguarde a configuração.  
3. Para compilar, pressione `F7` (**Build Project**).  
4. O arquivo `.uf2` será gerado automaticamente na pasta de build.  

## 📜 Como funciona  

1. O **botão** está conectado ao **pino GP5** e configurado como **entrada com pull-up**.  
2. O **buzzer** está conectado ao **pino GP21** e utiliza **PWM** para gerar som.  
3. Quando o botão é pressionado, o buzzer emite um **bipe de 1 segundo**.  
4. O código usa a biblioteca **pico/stdlib.h** para controle do GPIO e PWM.  

## 🔌 Esquema de ligação  

| Componente | Pino no Pico | Descrição |
|------------|------------|------------|
| **Botão** | GP5 | Entrada digital com pull-up interno |
| **Buzzer** | GP21 | Saída PWM para gerar som |

📌 **Importante**: Se estiver usando um **buzzer passivo**, a frequência pode ser ajustada na macro `#define BUZZER_FREQUENCY 100`.  

## 📥 Compilação e Upload  

1. **Compile o projeto** (`F7` no VS Code).  
2. O arquivo `.uf2` será gerado automaticamente.  
3. **Conecte o Pico no modo BOOTSEL** (`Segure o botão BOOTSEL e conecte via USB`).  
4. No VS Code, pressione `F5` (**Flash to Pico**).  
5. O código será carregado no Pico automaticamente! 🚀  

## 🚀 Expansões  

- Alterar a frequência do **PWM** para mudar o tom do som.  
- Adicionar diferentes padrões de **bipes** para diferentes eventos.  
- Integrar com **outros sensores ou LEDs** para um projeto mais avançado.  

---