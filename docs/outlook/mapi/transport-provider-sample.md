---
title: Exemplo de provedor de transporte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec6eb6c0-bfe3-4989-9071-89a14c0e7bdd
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1d0538f02f852580c064560460bb8b2ba54a2f65
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770661"
---
# <a name="transport-provider-sample"></a>Exemplo de provedor de transporte

  
  
**Aplica-se a**: Outlook 
  
Este exemplo usa os arquivos e diretórios para transmitir e receber mensagens. Ela implementa e registra um pré-processador muito simple que acrescenta uma linha de texto a cada mensagem de saída. O exemplo ilustra como dividir o conteúdo da mensagem entre TNEF Transport Neutral Encapsulation Format () e o texto. Ele também oferece suporte a todas as opções de configuração (folhas de propriedades, assistentes e configuração programática) e opções de mensagem. Ele não suporta as interfaces de transporte remoto. 
  
Você pode baixar esse exemplo de [Amostras de código do Outlook Messaging API (MAPI)](http://go.microsoft.com/fwlink/?LinkId=129740).
  
|||
|:-----|:-----|
|Executável:  <br/> |mrxp32.dll  <br/> |
|Diretório de origem do código:  <br/> |SampleTransportProvider\MRXP  <br/> |
|Idioma:  <br/> |C++  <br/> |
|Plataformas:  <br/> |Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 e Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Recursos compatíveis

Este exemplo aceita os seguintes recursos:
  
- Recursos básicos como enviar, receber e sondagem de novas mensagens.
    
- Configuração interativa e programática.
    
- A interface **IMAPIStatus** , exceto para a configuração da propriedade. Para obter mais informações, consulte o [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interface. 
    
- Acesso thread-safe.
    
- Log de eventos para um arquivo de texto. O arquivo está limitado automaticamente em um tamanho especificado. Todas as sessões de transporte usam o mesmo arquivo.
    
## <a name="unsupported-features"></a>Recursos sem suporte

Este exemplo não oferece suporte a detecção assíncrona de mensagens de entrada.
  
 **Para instalar o provedor de transporte de amostra**
  
1. Para baixar o provedor de transporte de amostra, consulte [Baixando as amostras de MAPI do Outlook](downloading-the-outlook-mapi-samples.md).
    
2. Localize a pasta onde você salvou as amostras de MAPI do Outlook. Com o botão direito do **OutlookMAPISamples -\<o número de versão\> ** zip pasta e clique em **Extrair tudo**.
    
3. Clique em **Procurar**, selecione o local onde deseja salvar a amostra e clique em **extrair**.
    
4. Execute o Visual Studio 2008.
    
5. No Visual Studio 2008, clique em **arquivo**, selecione **Abrir**e, em seguida, clique em **Project/Solution**.
    
6. Navegue até o local onde você salvou a amostra, clique em **mrxp32.vcproj**e, em seguida, clique em **Abrir**.
    
7. No menu **Build** , clique em **Gerenciador de configuração**.
    
8. Na caixa de diálogo **Gerenciador de configuração** , vá para a linha de **mrxp32** , na coluna **configuração** , selecione **versão**e, em seguida, clique em **Fechar**.
    
9. On the **Build** menu, click **Build Solution**.
    
10. Na caixa de diálogo **Salvar arquivo como** , clique em **Salvar**.
    
11. Na pasta onde você salvou a amostra, clique com o botão o arquivo de lote de instalação e clique em **Executar como administrador**.
    
12. Na caixa de diálogo **Controle de conta de usuário** , clique em **continuar**.
    
    > [!NOTE]
    > **Install. bat** copia o arquivo. dll na pasta de instalação do Microsoft Office padrão, C:\Program Files\Microsoft Office\Office12\. Se você tiver instalado os produtos do Office em um local diferente, clique com o botão **Install. bat** e clique em **Editar**. O arquivo será aberto no bloco de notas. Substitua o caminho de instalação padrão do caminho de instalação usado no seu computador. 
  
 **Para configurar o provedor de transporte no Outlook**
  
1. No menu **Ferramentas** do Outlook, clique em **Configurações de conta**.
    
2. Na caixa de diálogo **Configurações de conta** , na guia **Email** , clique em **novo**.
    
3. Em **Escolher serviço de Email** clique em **outros**, selecione **Transporte de amostra MRXP**e clique em **Avançar**.
    
4. Na caixa de diálogo **Configuração de transporte MRXP** digite um **Nome de exibição do usuário**.
    
5. Em **caminho para a caixa de entrada (compartilhamento UNC)** Insira um caminho de pasta. Isso também pode ser um caminho para uma pasta local. 
    
    > [!IMPORTANT]
    > Esse caminho deve existir. 
  
6. Clique em **OK**.
    
7. Na caixa de diálogo **Adicionar conta de Email** , clique em **Okey**. Clique em **Concluir** e clique em **Fechar**.
    
8. Para começar a usar a conta MRXP, saia e reinicie o Outlook.
    
 **Usar o exemplo de provedor de transporte para enviar uma mensagem no Outlook**
  
1. No menu **arquivo** , clique em **novo**e, em seguida, clique em **Email**.
    
2. Na caixa **para** , digite o nome do destinatário usando o formato **[MRXP:\<endereço\>]**. O endereço é o compartilhamento UNC ou o caminho da pasta local na caixa de entrada do destinatário.
    
    > [!NOTE]
    > Se houver dois pontos ou barras invertidas no endereço, você deve inserir uma barra invertida antes de cada dois-pontos ou barra invertida. Por exemplo, para enviar email para [MRXP:C:\Mail\myDir] deverá digitar `[MRXP:C\:\\Mail\\myDir]`. 
  
    > [!IMPORTANT]
    > O endereço do destinatário deve existir. 
  
3. Clique na **conta** e clique em **MRXP amostra transporte**.
    
4. Digite sua mensagem e clique em **Enviar**. A mensagem é enviada usando o provedor de transporte MRXP.
    
 **Usar o exemplo de provedor de transporte para receber uma mensagem no Outlook**
  
1. No menu **arquivo** , clique em **novo**e, em seguida, clique em **Email**.
    
2. Digite sua mensagem.
    
3. Clique no **Botão do Microsoft Office**, clique em **Salvar como**e, em seguida, clique em **Salvar como** para salvar o arquivo para a pasta de entrada especificada durante a instalação. 
    
4. Na caixa de diálogo **Salvar como** , navegue até o compartilhamento UNC ou uma pasta local que você definiu como sua caixa de entrada. 
    
5. Na lista suspensa **Salvar como tipo** , clique em **Formato de mensagem do Outlook**.
    
6. Digite um nome para o arquivo e clique em **Salvar**.
    
7. O arquivo é salvo na pasta compartilhada. O provedor de transporte MRXP entrega a mensagem para sua caixa de entrada no Outlook.
    

