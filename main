import streamlit as st

st.set_page_config(
    page_title="Dani Nutri IA",
    page_icon="💛",
    layout="centered"
)

st.markdown("""
    <style>
    .main {
        background-color: #f8f4ef;
    }

    .title {
        text-align: center;
        font-size: 42px;
        font-weight: bold;
        color: #333333;
    }

    .subtitle {
        text-align: center;
        font-size: 18px;
        color: #777777;
        margin-bottom: 30px;
    }

    .stButton > button {
        width: 100%;
        background-color: #fb923c;
        color: white;
        border-radius: 14px;
        border: none;
        padding: 14px;
        font-size: 18px;
        font-weight: bold;
    }
    </style>
""", unsafe_allow_html=True)

st.markdown('<div class="title">💛 Dani Nutri IA</div>', unsafe_allow_html=True)
st.markdown('<div class="subtitle">Seu acompanhamento alimentar inteligente e humano</div>', unsafe_allow_html=True)

with st.form("anamnese_form"):

    st.subheader("📋 Anamnese Inicial")

    nome = st.text_input("Nome completo")

    col1, col2, col3 = st.columns(3)

    with col1:
        idade = st.number_input("Idade", min_value=10, max_value=100)

    with col2:
        peso = st.number_input("Peso (kg)", min_value=30.0, max_value=300.0)

    with col3:
        altura = st.number_input("Altura (cm)", min_value=100, max_value=250)

    objetivo = st.selectbox(
        "Objetivo",
        [
            "Emagrecimento",
            "Manutenção",
            "Ganho de massa",
            "Alimentação saudável"
        ]
    )

    st.subheader("🏋️ Atividade Física")

    frequencia = st.selectbox(
        "Frequência de treino",
        [
            "Não pratico",
            "1 a 2x por semana",
            "3 a 5x por semana",
            "Treino diariamente"
        ]
    )

    atividade = st.text_input(
        "Qual atividade física você pratica?",
        placeholder="Ex: musculação, caminhada, corrida..."
    )

    duracao = st.selectbox(
        "Duração média do treino",
        [
            "Menos de 30 minutos",
            "30 a 45 minutos",
            "45 a 60 minutos",
            "Mais de 1 hora"
        ]
    )

    st.subheader("🍽️ Rotina Alimentar")

    rotina_alimentar = st.text_area(
        "Como é sua rotina alimentar?",
        placeholder="Conte como costuma ser sua alimentação no dia a dia, os horários que geralmente come e se costuma pular refeições"
    )

    st.subheader("💛 Saúde & Bem-estar")

    ansiedade = st.selectbox(
        "Você sente ansiedade ou compulsão alimentar?",
        [
            "Não",
            "Às vezes",
            "Com frequência"
        ]
    )

    condicoes = st.multiselect(
        "Você possui alguma condição de saúde?",
        [
            "Gastrite",
            "Diabetes",
            "Intestino preso",
            "Intestino solto",
            "Ansiedade",
            "Compulsão alimentar",
            "Hipertireoidismo"
        ]
    )

    col4, col5 = st.columns(2)

    with col4:
        acorda = st.time_input("Que horas você acorda?")

    with col5:
        dorme = st.time_input("Que horas costuma dormir?")

    sono = st.number_input(
        "Quantas horas você dorme por noite?",
        min_value=0,
        max_value=24
    )

    cansado = st.selectbox(
        "Você costuma acordar cansado(a)?",
        [
            "Não",
            "Às vezes",
            "Frequentemente"
        ]
    )

    rotina_trabalho = st.text_area(
        "Como é sua rotina de trabalho?",
        placeholder="Ex: trabalho sentado, rotina corrida, muito tempo fora de casa..."
    )

    desafio = st.selectbox(
        "Qual seu maior desafio hoje?",
        [
            "Ansiedade alimentar",
            "Falta de tempo",
            "Vontade de doce",
            "Falta de disciplina",
            "Compulsão alimentar"
        ]
    )

    gosta = st.text_area(
        "Alimentos que você gosta",
        placeholder="Ex: frutas, arroz, massas, chocolate..."
    )

    nao_gosta = st.text_area(
        "Alimentos que você não gosta ou não comeria",
        placeholder="Ex: peixe, cebola, fígado..."
    )

    enviar = st.form_submit_button("Começar meu acompanhamento 💛")

if enviar:

    st.success("Anamnese enviada com sucesso 💛")

    st.subheader("📊 Resumo do Cadastro")

    st.write(f"**Nome:** {nome}")
    st.write(f"**Objetivo:** {objetivo}")
    st.write(f"**Atividade Física:** {atividade}")
    st.write(f"**Frequência:** {frequencia}")
    st.write(f"**Maior desafio:** {desafio}")

    st.info(
        "Em breve sua IA irá calcular automaticamente calorias, macros e acompanhar suas refeições 🍽️"
    )
