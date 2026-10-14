
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Saieed Davis | Personal Medical Record</title>

<style>
:root {
    --blue: #2563eb;
    --blue-light: #eff6ff;
    --purple: #7c3aed;
    --purple-light: #f5f3ff;
    --white: #ffffff;
    --background: #f5f7fc;
    --text: #26334d;
    --muted: #718096;
    --border: #e3e9f4;
}

* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: "Segoe UI", Arial, sans-serif;
    background: var(--background);
    color: var(--text);
    line-height: 1.6;
}

header {
    background: linear-gradient(120deg, var(--blue), var(--purple));
    color: white;
    padding: 30px 6%;
}

.header-top {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 15px;
}

.brand {
    font-weight: 700;
    font-size: 20px;
}

.controls {
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
}

select, button {
    border: none;
    border-radius: 9px;
    padding: 10px 14px;
    font: inherit;
    cursor: pointer;
}

select {
    color: var(--text);
    background: white;
}

.profile {
    display: flex;
    align-items: center;
    gap: 20px;
    margin-top: 35px;
}

.avatar {
    width: 85px;
    height: 85px;
    display: grid;
    place-items: center;
    flex-shrink: 0;
    border-radius: 24px;
    background: rgba(255,255,255,.2);
    border: 1px solid rgba(255,255,255,.5);
    font-size: 30px;
    font-weight: 800;
}

.profile h1 {
    font-size: clamp(25px, 4vw, 36px);
    margin-bottom: 5px;
}

.profile p {
    opacity: .9;
}

main {
    max-width: 1150px;
    margin: 30px auto;
    padding: 0 22px;
}

.notice {
    background: var(--purple-light);
    border-left: 4px solid var(--purple);
    border-radius: 10px;
    padding: 15px;
    margin-bottom: 24px;
    font-size: 14px;
}

.section-heading {
    font-size: 20px;
    margin-bottom: 17px;
    color: var(--blue);
}

.grid {
    display: grid;
    grid-template-columns: repeat(12, minmax(0, 1fr));
    gap: 20px;
}

.card {
    background: var(--white);
    border: 1px solid var(--border);
    border-radius: 17px;
    padding: 24px;
    box-shadow: 0 5px 20px rgba(37, 99, 235, .045);
    min-width: 0;
}

.span-8 { grid-column: span 8; }
.span-4 { grid-column: span 4; }
.span-6 { grid-column: span 6; }
.span-12 { grid-column: span 12; }

.info-row {
    display: grid;
    grid-template-columns: minmax(100px, .7fr) minmax(0, 1.5fr);
    gap: 12px;
    padding: 11px 0;
    border-bottom: 1px solid #edf0f7;
}

.info-row:last-child {
    border-bottom: none;
}

.label {
    color: var(--muted);
    font-size: 14px;
}

.value {
    font-weight: 600;
    overflow-wrap: anywhere;
}

.metrics {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 10px;
}

.metric {
    background: var(--blue-light);
    border-radius: 12px;
    padding: 15px 10px;
    text-align: center;
}

.metric:nth-child(2) {
    background: var(--purple-light);
}

.metric small {
    display: block;
    color: var(--muted);
    font-size: 12px;
}

.metric strong {
    display: block;
    margin-top: 5px;
    color: var(--blue);
    font-size: 19px;
}

.badge {
    display: inline-block;
    border-radius: 20px;
    padding: 5px 12px;
    background: #e9f9ef;
    color: #187744;
    font-size: 13px;
    font-weight: 700;
}

.history {
    border-left: 4px solid var(--purple);
    padding: 5px 0 5px 15px;
}

.history p {
    color: var(--muted);
    margin-top: 5px;
    font-size: 14px;
}

.emergency {
    background: linear-gradient(135deg, #eff6ff, #f5f3ff);
    border-color: #d9ddff;
}

.actions {
    display: flex;
    gap: 12px;
    flex-wrap: wrap;
    margin-top: 20px;
}

.btn-primary {
    background: var(--blue);
    color: white;
}

.btn-secondary {
    background: var(--purple);
    color: white;
}

footer {
    text-align: center;
    color: var(--muted);
    padding: 10px 20px 30px;
    font-size: 13px;
}

@media (max-width: 760px) {
    .span-8, .span-4, .span-6 {
        grid-column: span 12;
    }

    .profile {
        align-items: flex-start;
    }

    .card {
        padding: 19px;
    }
}

@media (max-width: 430px) {
    .metrics {
        grid-template-columns: 1fr;
    }

    .info-row {
        grid-template-columns: 1fr;
        gap: 2px;
    }

    .avatar {
        width: 62px;
        height: 62px;
        border-radius: 17px;
    }
}

@media print {
    body {
        background: white;
    }

    header {
        background: #2563eb !important;
        color: white !important;
        print-color-adjust: exact;
        -webkit-print-color-adjust: exact;
    }

    .controls, .actions {
        display: none !important;
    }

    main {
        margin-top: 15px;
    }

    .card {
        box-shadow: none;
        break-inside: avoid;
    }
}
</style>
</head>

<body>

<header>
    <div class="header-top">
        <div class="brand" data-en="✚ Personal Health Record"
             data-zh="✚ 個人健康紀錄"
             data-es="✚ Registro Personal de Salud">
            ✚ Personal Health Record
        </div>

        <div class="controls">
            <select id="language" aria-label="Choose language">
                <option value="en">English</option>
                <option value="zh">繁體中文</option>
                <option value="es">Español</option>
            </select>
            <button onclick="window.print()" data-en="Print / Save PDF"
                    data-zh="列印／儲存 PDF"
                    data-es="Imprimir / Guardar PDF">
                Print / Save PDF
            </button>
        </div>
    </div>

    <div class="profile">
        <div class="avatar">SR</div>
        <div>
            <h1>Saieed R Davis</h1>
            <p data-en="Personal Medical Summary"
               data-zh="個人醫療摘要"
               data-es="Resumen Médico Personal">
                Personal Medical Summary
            </p>
            <p style="margin-top:8px;font-size:13px"
               data-en="Patient-held record • Updated October 2026"
               data-zh="個人保存紀錄 • 更新於 2026 年 10 月"
               data-es="Registro personal • Actualizado en octubre de 2026">
                Patient-held record • Updated October 2026
            </p>
        </div>
    </div>
</header>

<main>
    <div class="notice">
        <strong data-en="Privacy notice: "
                data-zh="隱私提醒："
                data-es="Aviso de privacidad: ">Privacy notice: </strong>
        <span data-en="This is a personal reference record, not an official hospital EHR. Information is stored in this HTML file; keep it private and secure."
              data-zh="此為個人參考紀錄，並非正式醫院電子病歷。資料儲存在此 HTML 檔案中，請妥善保密。"
              data-es="Este es un registro personal de referencia, no una historia clínica hospitalaria oficial. La información está guardada en este archivo HTML; manténgalo seguro.">
            This is a personal reference record, not an official hospital EHR. Information is stored in this HTML file; keep it private and secure.
        </span>
    </div>

    <div class="grid">

        <section class="card span-8">
            <h2 class="section-heading" data-en="👤 Patient Information"
                data-zh="👤 患者資料"
                data-es="👤 Información del Paciente">👤 Patient Information</h2>

            <div class="info-row">
                <span class="label" data-en="Full name" data-zh="全名" data-es="Nombre completo">Full name</span>
                <span class="value">Saieed R Davis</span>
            </div>
            <div class="info-row">
                <span class="label" data-en="Age" data-zh="年齡" data-es="Edad">Age</span>
                <span class="value" data-en="31 years" data-zh="31 歲" data-es="31 años">31 years</span>
            </div>
            <div class="info-row">
                <span class="label" data-en="Ethnicity" data-zh="族裔" data-es="Etnia">Ethnicity</span>
                <span class="value" data-en="Afro-Caribbean" data-zh="非裔加勒比海裔" data-es="Afrocaribeño">Afro-Caribbean</span>
            </div>
            <div class="info-row">
                <span class="label" data-en="Address" data-zh="地址" data-es="Dirección">Address</span>
                <span class="value">Yuantong Dormitory, No. 26-38號, Gongzhuan Rd, Huaxin Village, Zhonghe District, New Taipei City, Taiwan 235</span>
            </div>
        </section>

        <section class="card span-4">
            <h2 class="section-heading" data-en="📊 Measurements"
                data-zh="📊 身體測量"
                data-es="📊 Medidas">📊 Measurements</h2>

            <div class="metrics">
                <div class="metric">
                    <small data-en="Weight" data-zh="體重" data-es="Peso">Weight</small>
                    <strong>154 kg</strong>
                </div>
                <div class="metric">
                    <small data-en="Height" data-zh="身高" data-es="Altura">Height</small>
                    <strong>6 ft</strong>
                </div>
                <div class="metric">
                    <small data-en="Blood type" data-zh="血型" data-es="Grupo sanguíneo">Blood type</small>
                    <strong>O Rh+</strong>
                </div>
            </div>
            <p style="color:var(--muted);font-size:12px;margin-top:13px"
               data-en="Patient-reported values. Confirm blood type clinically before treatment."
               data-zh="由患者提供的資料。治療前請以正式檢驗確認血型。"
               data-es="Datos informados por el paciente. Confirme el grupo sanguíneo clínicamente antes del tratamiento.">
                Patient-reported values. Confirm blood type clinically before treatment.
            </p>
        </section>

        <section class="card span-6">
            <h2 class="section-heading" data-en="🩺 Medical History"
                data-zh="🩺 病史"
                data-es="🩺 Antecedentes Médicos">🩺 Medical History</h2>
            <div class="history">
                <strong data-en="Bronchopneumonia — 2025"
                        data-zh="支氣管肺炎 — 2025 年"
                        data-es="Bronconeumonía — 2025">Bronchopneumonia — 2025</strong>
                <p data-en="Previous condition reported by the patient."
                   data-zh="由患者提供的既往病史。"
                   data-es="Antecedente informado por el paciente.">
                    Previous condition reported by the patient.
                </p>
            </div>
        </section>

        <section class="card span-6">
            <h2 class="section-heading" data-en="🏥 Surgical History"
                data-zh="🏥 手術史"
                data-es="🏥 Antecedentes Quirúrgicos">🏥 Surgical History</h2>
            <p data-en="No surgical history reported."
               data-zh="未提供手術史。"
               data-es="No se han informado cirugías.">No surgical history reported.</p>

            <h2 class="section-heading" style="margin-top:22px"
                data-en="💊 Current Medication"
                data-zh="💊 目前用藥"
                data-es="💊 Medicamentos Actuales">💊 Current Medication</h2>
            <span class="badge" data-en="None reported"
                  data-zh="未提供／無"
                  data-es="Ninguno informado">None reported</span>
        </section>

        <section class="card span-6">
            <h2 class="section-heading" data-en="⚕️ Allergies"
                data-zh="⚕️ 過敏史"
                data-es="⚕️ Alergias">⚕️ Allergies</h2>
            <span class="badge" data-en="No known allergies reported"
                  data-zh="未提供已知過敏"
                  data-es="No se informan alergias conocidas">No known allergies reported</span>
            <p style="color:var(--muted);font-size:13px;margin-top:12px"
               data-en="Inform healthcare professionals about any previous allergic reactions."
               data-zh="若曾有過敏反應，請告知醫療人員。"
               data-es="Informe al personal sanitario sobre cualquier reacción alérgica previa.">
                Inform healthcare professionals about any previous allergic reactions.
            </p>
        </section>

        <section class="card span-6 emergency">
            <h2 class="section-heading" data-en="🚨 Emergency Contact"
                data-zh="🚨 緊急聯絡人"
                data-es="🚨 Contacto de Emergencia">🚨 Emergency Contact</h2>

            <div class="info-row">
                <span class="label" data-en="Next of kin" data-zh="近親／聯絡人" data-es="Familiar de contacto">Next of kin</span>
                <span class="value">Sandra Davis</span>
            </div>
            <div class="info-row">
                <span class="label" data-en="Phone" data-zh="電話" data-es="Teléfono">Phone</span>
                <span class="value"><a href="tel:+17844554477">+1 784 455 4477</a></span>
            </div>
        </section>

        <section class="card span-12">
            <h2 class="section-heading" data-en="📋 Record Notes"
                data-zh="📋 紀錄備註"
                data-es="📋 Notas del Registro">📋 Record Notes</h2>

            <p data-en="This personal summary has been prepared from information supplied by the patient. It has not been independently verified by a healthcare professional. Update the record whenever your medical information changes."
               data-zh="本摘要依患者提供的資訊製作，尚未由醫療專業人員獨立核實。醫療資訊變更時請更新。"
               data-es="Este resumen se preparó con información proporcionada por el paciente y no ha sido verificado de forma independiente por un profesional sanitario. Actualícelo cuando cambie su información médica.">
                This personal summary has been prepared from information supplied by the patient. It has not been independently verified by a healthcare professional. Update the record whenever your medical information changes.
            </p>

            <div class="actions">
                <button class="btn-primary" onclick="window.print()"
                        data-en="Print / Save PDF"
                        data-zh="列印／儲存 PDF"
                        data-es="Imprimir / Guardar PDF">Print / Save PDF</button>
                <button class="btn-secondary" onclick="copyContact()"
                        data-en="Copy Emergency Contact"
                        data-zh="複製緊急聯絡資料"
                        data-es="Copiar Contacto">Copy Emergency Contact</button>
                <span id="copy-status" role="status" aria-live="polite"></span>
            </div>
        </section>

    </div>
</main>

<footer data-en="Personal Health Record • Keep your medical information private."
        data-zh="個人健康紀錄 • 請妥善保護您的醫療資料。"
        data-es="Registro Personal de Salud • Mantenga privada su información médica.">
    Personal Health Record • Keep your medical information private.
</footer>

<script>
const language = document.getElementById("language");

language.addEventListener("change", function () {
    const lang = this.value;

    document.documentElement.lang =
        lang === "zh" ? "zh-Hant" : lang;

    document.querySelectorAll("[data-" + lang + "]").forEach(function (element) {
        element.textContent = element.getAttribute("data-" + lang);
    });
});

async function copyContact() {
    const contact = "Sandra Davis — Next of kin — +17844554477";
    const status = document.getElementById("copy-status");

    try {
        await navigator.clipboard.writeText(contact);
        status.textContent = "Copied!";
    } catch (error) {
        status.textContent = contact;
    }
}
</script>

</body>
</html>
