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
ms.openlocfilehash: def51a752abcb79a35980ed12eb73011c26d2597
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356585"
---
# <a name="transport-provider-sample"></a>Exemplo de provedor de transporte

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este exemplo usa arquivos e diretórios para transmitir e receber mensagens. Ele implementa e registra um pré-processador muito simples que acrescenta uma linha de texto a cada mensagem de saída. O exemplo ilustra como dividir o conteúdo de mensagens entre o formato de encapsulamento (TNEF) de transporte neutro e o texto. Também oferece suporte a todas as opções de configuração (folhas de propriedades, assistentes e configuração programática) e opções de mensagem. Ele não é compatível com as interfaces de transporte remoto. 
  
Você pode baixar esse exemplo de [exemplos de código da API de mensagens do Outlook (MAPI)](https://go.microsoft.com/fwlink/?LinkId=129740).
  
|||
|:-----|:-----|
|Arquivo  <br/> |mrxp32. dll  <br/> |
|Diretório do código-fonte:  <br/> |SampleTransportProvider\MRXP  <br/> |
|Pacote  <br/> |C++  <br/> |
|Plataformas  <br/> |Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 e Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Recursos com suporte

Este exemplo oferece suporte aos seguintes recursos:
  
- Recursos básicos como enviar, receber e sondar novas mensagens.
    
- Configuração interativa e programática.
    
- A interface **IMAPIStatus** , exceto a configuração da propriedade. Para obter mais informações, consulte a interface [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) . 
    
- Segurança de thread.
    
- Log de eventos em um arquivo de texto. O arquivo é automaticamente limitado a um tamanho especificado. Todas as sessões de transporte usam o mesmo arquivo.
    
## <a name="unsupported-features"></a>Recursos sem suporte

Este exemplo não dá suporte à detecção assíncrona de mensagens de entrada.
  
 **Para instalar o provedor de transporte de amostra**
  
1. Para baixar o provedor de transporte de exemplo, confira [download dos exemplos de MAPI do Outlook](downloading-the-outlook-mapi-samples.md).
    
2. Localize a pasta onde você salvou os exemplos de MAPI do Outlook. Clique com o botão direito do mouse na pasta zip **OutlookMAPISamples número\<\> de versão** e clique em **extrair tudo**.
    
3. Clique em **procurar**, selecione o local onde deseja salvar o exemplo e clique em **extrair**.
    
4. Execute o Visual Studio 2008.
    
5. No Visual Studio 2008, clique em **arquivo**, selecione **abrir**e, em seguida, clique em **projeto/solução**.
    
6. Navegue até o local onde você salvou o exemplo, clique em **mrxp32. vcproj**e, em seguida, clique em **abrir**.
    
7. No menu **criar** , clique em **Gerenciador de configurações**.
    
8. Na caixa de diálogo **Gerenciador de configurações** , vá para a linha **mrxp32** e, na coluna **configuração** , selecione **liberar**e clique em **fechar**.
    
9. On the **Build** menu, click **Build Solution**.
    
10. Na caixa de diálogo **salvar arquivo como** , clique em **salvar**.
    
11. Na pasta onde você salvou o exemplo, clique com o botão direito do mouse no arquivo em lotes de instalação e clique em **Executar como administrador**.
    
12. Na caixa de diálogo **Controle de Conta de Usuário**, clique em **Continuar**.
    
    > [!NOTE]
    > **install. bat** copia o. dll para a pasta de instalação padrão do Microsoft Office, C:\Arquivos de Programas\Microsoft Office\OFFICE12\. Se você tiver instalado os produtos do Office em um local diferente, clique com o botão direito em **instalar. bat** e clique em **Editar**. O arquivo é aberto no bloco de notas. Substitua o caminho de instalação padrão pelo caminho de instalação usado no computador. 
  
 **Para configurar o provedor de transporte no Outlook**
  
1. No menu **ferramentas** do Outlook, clique em **configurações de conta**.
    
2. Na caixa de diálogo **configurações da conta** , na guia **email** , clique em **novo**.
    
3. Em **escolher serviço de email** , clique em **outros**, selecione **MRXP transporte de exemplo**e clique em **Avançar**.
    
4. Na caixa de diálogo **MRXP Transport Configuration** digite um **nome de exibição do usuário**.
    
5. Em **caminho para caixa de entrada (compartilhamento UNC)** , insira um caminho de pasta. Também pode ser um caminho para uma pasta local. 
    
    > [!IMPORTANT]
    > Este caminho deve existir. 
  
6. Clique em **OK**.
    
7. Na caixa de diálogo **adicionar conta de email** , clique em **OK**. Clique em **concluir** e, em seguida, clique em **fechar**.
    
8. Para começar a usar a conta MRXP, saia e reinicie o Outlook.
    
 **Para usar o exemplo de provedor de transporte para enviar uma mensagem no Outlook**
  
1. No menu **arquivo** , clique em **novo**e em mensagem de **email**.
    
2. Na caixa **para** , digite o nome do destinatário usando o formato **[MRXP:\<\>endereço]**. O endereço é o compartilhamento UNC ou caminho de pasta local para a caixa de entrada do destinatário.
    
    > [!NOTE]
    > Se houver dois-pontos ou barras invertidas no endereço, você deverá inserir uma barra invertida antes de cada dois-pontos ou barra invertida. Por exemplo, para enviar emails para [MRXP: C: \Mail\myDir] você deve `[MRXP:C\:\\Mail\\myDir]`digitar. 
  
    > [!IMPORTANT]
    > O endereço do destinatário deve existir. 
  
3. Clique em **conta** e em **MRXP de amostra de transporte**.
    
4. Digite sua mensagem e clique em **Enviar**. A mensagem é enviada usando o provedor de transporte MRXP.
    
 **Para usar o exemplo de provedor de transporte para receber uma mensagem no Outlook**
  
1. No menu **arquivo** , clique em **novo**e em mensagem de **email**.
    
2. Digite sua mensagem.
    
3. Clique no **botão do Microsoft Office**, clique em **salvar como**e, em seguida, clique em **salvar como** para salvar o arquivo na pasta de caixa de entrada especificada durante a instalação. 
    
4. Na caixa de diálogo **salvar como** , navegue até o compartilhamento UNC ou a pasta local que você definiu como caixa de entrada. 
    
5. Na lista suspensa **salvar como tipo** , clique em **formato de mensagem do Outlook**.
    
6. Digite um nome para o arquivo e clique em **salvar**.
    
7. O arquivo é salvo na pasta compartilhada. O provedor de transporte do MRXP entrega a mensagem para sua caixa de entrada no Outlook.
    

