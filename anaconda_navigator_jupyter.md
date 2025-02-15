# Anaconda

Se não queres que o `(base)` apareça automaticamente sempre que abres o terminal, o **recomendado** é desativar essa ativação automática. Assim, podes ativar manualmente o ambiente sempre que precisares.  

### 🔹 **Passos Recomendados**  

#### 1️⃣ **Desativar a ativação automática do ambiente `base`**  
No terminal, executa:  
```bash
conda config --set auto_activate_base false
```
🔹 **Isto impede que o `(base)` apareça sempre no terminal.**

#### 2️⃣ **Fechar e reabrir o terminal**  
Depois de executar o comando acima, fecha o terminal e abre um novo. Agora o `(base)` **não aparecerá automaticamente**.

---

### 🔹 **Como ativar um ambiente quando precisares?**  
Se precisares de usar o Anaconda, podes ativar o ambiente manualmente:  
- Para ativar o ambiente `base`:  
  ```bash
  conda activate base
  ```
-- Para abrir o Anaconda Navigator, é necessário ativar o ambiente primeiro (comando acima ou outro que especifique o ambiente). Depois, executa:  
  ```bash
  anaconda-navigator
  ```
- Para ativar um ambiente específico (exemplo: `meu_ambiente` com Python 3.10):  
  ```bash
  conda activate meu_ambiente
  ```

Se quiseres voltar ao estado original (onde o `(base)` ativa automaticamente), basta reverter:  
```bash
conda config --set auto_activate_base true
```

Desta forma, tens mais controlo e evitas que o `(base)` fique sempre ativo sem necessidade.


# Anaconda com Python < 3.11

## **Instalar uma Versão de Python < 3.11**  
Se a versão do Python instalada for superior a 3.11, precisas de criar um ambiente virtual com uma versão mais antiga:  

1. **Abre o Anaconda Prompt** (ou Terminal no Linux).  
2. Cria um novo ambiente com Python 3.10:  
   ```bash
   conda create --name meu_ambiente python=3.10
   ```  
3. Ativa o ambiente:  
   - **Linux**:  
     ```bash
     source <PATH_TO_CONDA>/bin/activate meu_ambiente ---> source ~/anaconda3/bin/activate meu_ambiente  OR conda activate meu_ambiente
     ```  
     To deactivate:  
     ```bash
      conda deactivate
      ```
4. Instala o Jupyter Notebook dentro deste ambiente:  
   ```bash
   conda install jupyter  
   ```  
5. Para testar, executa:  
   ```bash
   jupyter notebook
   ```  
   Se abrir no browser, está pronto!   

Sempre que fores às aulas, lembra-te de **ativar o ambiente** antes de abrir o Jupyter.  


# Remover um Ambiente

Para eliminar completamente o ambiente `meu_ambiente`, segue estes passos:  

### 1️⃣ **Certificar que o ambiente não está ativo**  
Primeiro, se estás dentro do ambiente que queres eliminar, **sai dele** antes de prosseguir:  
```bash
conda deactivate
```

### 2️⃣ **Remover o ambiente**  
Agora, para eliminar o ambiente `meu_ambiente`, usa o seguinte comando:  
```bash
conda env remove --name meu_ambiente
```
Isto apaga todos os pacotes e configurações associadas a esse ambiente.  

### 3️⃣ **Confirmar que foi eliminado**  
Para verificar se o ambiente foi removido com sucesso, lista os ambientes disponíveis:  
```bash
conda env list
```
ou  
```bash
conda info --envs
```
Se `meu_ambiente` não aparecer na lista, então foi eliminado com sucesso. 