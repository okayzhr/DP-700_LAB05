# DP-700_LAB05
# Microsoft Fabric: Dataflows (Gen2) gebruiken

Dit project laat zien hoe je Dataflows (Gen2) kunt gebruiken binnen Microsoft Fabric om gegevens op te halen, transformeren en laden in een Lakehouse-omgeving.

## 🧪 Labdoel

Leer de basiselementen van Dataflows (Gen2) kennen in Microsoft Fabric door:
- Een workspace aan te maken
- Een lakehouse te creëren
- Gegevens in te laden via een Dataflow (Gen2)
- Een data pipeline op te zetten met een dataflow-activiteit

> 🕒 Duur: Ongeveer 30 minuten  
> ⚠️ Vereist: Microsoft Fabric Trial-account

---

## 📁 1. Workspace aanmaken

1. Ga naar [Microsoft Fabric](https://app.fabric.microsoft.com/home?experience=fabric) en meld je aan.
2. Navigeer naar **Workspaces** en klik op **Nieuwe workspace**.
3. Geef een naam en kies een licentie met Fabric-capaciteit (Trial, Premium, of Fabric).

---

## 🏠 2. Lakehouse maken

1. Klik op **Create** > **Lakehouse** onder het gedeelte *Data Engineering*.
2. Geef een unieke naam en wacht tot het lakehouse is aangemaakt.

---

## 📄 3. Dataflow (Gen2) maken en configureren

1. Klik op **Get data** > **New Dataflow Gen2**.
2. Kies **Import from Text/CSV** met de volgende instellingen:
   - URL: `https://raw.githubusercontent.com/MicrosoftLearning/dp-data/main/orders.csv`
   - Authenticatie: Anoniem
3. Voeg een aangepaste kolom toe:
   - Kolomnaam: `MonthNo`
   - Type: Geheel Getal
   - Formule: `Date.Month([OrderDate])`
4. Zorg dat `OrderDate` als *Date* is getypeerd en `MonthNo` als *Whole Number*.

---

## 📤 4. Doel instellen: Lakehouse

1. Klik op **Add data destination** > **Lakehouse**.
2. Meld je aan met je Power BI-organisatieaccount.
3. Kies je workspace en lakehouse.
4. Specificeer een nieuwe tabelnaam: `orders`.
5. Kies **Append** bij de instellingen en publiceer de dataflow.

---

## 🔁 5. Pipeline maken en uitvoeren

1. Maak een nieuwe **Data Pipeline** aan genaamd *Load data*.
2. Voeg een **Dataflow activity** toe en kies de eerder aangemaakte dataflow.
3. Sla de pipeline op en klik op **Run**.
4. Wacht tot het laden is voltooid.

---

## 🔍 6. Resultaat controleren

1. Ga naar het lakehouse en ververs de tabellen.
2. Open de tabel **orders** om de geladen gegevens te bekijken.

---

## 🧹 7. Opruimen

1. Ga naar je workspace-instellingen.
2. Scroll naar beneden en klik op **Remove this workspace** om alles te verwijderen.

---

## 📊 Extra

Je kunt deze dataflows direct gebruiken in Power BI Desktop via de connector **Power BI dataflows (Legacy)** voor verdere analyse en rapportage.

---

## 📌 Opmerking

Deze oefening is bedoeld als introductie en is geen vervanging voor een volledige enterprise-oplossing.


![Schermafbeelding 2025-04-30 085036](https://github.com/user-attachments/assets/31efb70f-7b87-42a6-9d70-96b4f0faf734)


![Schermafbeelding 2025-04-30 085320](https://github.com/user-attachments/assets/66dd2baf-0ecb-4358-8517-fdbc315940e1)




![Schermafbeelding 2025-04-30 085550](https://github.com/user-attachments/assets/cc904058-8bb3-4131-b292-9ea17af5e44c)


![Schermafbeelding 2025-04-30 085701](https://github.com/user-attachments/assets/2fa6e2aa-b292-409f-84c8-49c24a76bd01)

![Schermafbeelding 2025-04-30 085717](https://github.com/user-attachments/assets/96537a3f-dddc-4a5b-b7fe-c0b7a1100072)

![Schermafbeelding 2025-04-30 091821](https://github.com/user-attachments/assets/df62e691-2bf3-411a-8200-dca6ca186a24)



![Schermafbeelding 2025-04-30 092251](https://github.com/user-attachments/assets/ae072cd9-adcf-45cb-9ff6-129e4c3ed52f)


![Schermafbeelding 2025-04-30 092421](https://github.com/user-attachments/assets/4f8711fa-9221-4971-b570-cc615a659c64)


![Schermafbeelding 2025-04-30 092703](https://github.com/user-attachments/assets/7e4cb965-8ee6-4691-ae97-aa2e163038bb)



![Schermafbeelding 2025-04-30 093043](https://github.com/user-attachments/assets/f11cc87d-5b7b-41f5-990d-2f0f7aadb334)


![Schermafbeelding 2025-04-30 093326](https://github.com/user-attachments/assets/5b59432b-e57c-4820-bb62-5dc186259cb1)
![Schermafbeelding 2025-04-30 093503](https://github.com/user-attachments/assets/2202f94e-8a2f-4ac9-9d4e-63c08648c57f)



![Schermafbeelding 2025-04-30 093601](https://github.com/user-attachments/assets/54c59e4d-361a-4e5f-8db0-f0f75fdd094a)








