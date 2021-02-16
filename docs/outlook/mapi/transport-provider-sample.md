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
  
Este exemplo usa arquivos e diretórios para transmitir e receber mensagens. Ele implementa e registra um pré-processador muito simples que anexa uma linha de texto a cada mensagem de saída. O exemplo ilustra como dividir o conteúdo da mensagem entre o TNEF (Transport Neutral Encapsulation Format) e o texto. Ele também oferece suporte a todas as opções de configuração (folhas de propriedades, assistentes e configuração programática) e opções de mensagem. Ele não dá suporte às interfaces de transporte remoto. 
  
Você pode baixar este exemplo dos exemplos de código [da API de Mensagens do Outlook (MAPI).](https://go.microsoft.com/fwlink/?LinkId=129740)
  
|||
|:-----|:-----|
|Executável:  <br/> |mrxp32.dll  <br/> |
|Diretório do código-fonte:  <br/> |SampleTransportProvider\MRXP  <br/> |
|Idioma:  <br/> |C++  <br/> |
|Plataformas:  <br/> |Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 e Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Recursos com suporte

Este exemplo dá suporte aos seguintes recursos:
  
- Recursos básicos, como envio, recebimento e sondagem de novas mensagens.
    
- Configuração interativa e programática.
    
- A interface **IMAPIStatus,** exceto para a configuração da propriedade. Para obter mais informações, consulte a interface [IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md) 
    
- Segurança do thread.
    
- Log de eventos para um arquivo de texto. O arquivo é automaticamente limitado a um tamanho especificado. Todas as sessões de transporte usam o mesmo arquivo.
    
## <a name="unsupported-features"></a>Recursos sem suporte

Este exemplo não dá suporte à detecção assíncrona de mensagens de entrada.
  
 **Para instalar o Provedor de Transporte de Exemplo**
  
1. Para baixar o Provedor de Transporte de Exemplo, consulte [Baixando os exemplos de MAPI do Outlook.](downloading-the-outlook-mapi-samples.md)
    
2. Localize a pasta onde você salvou os exemplos de MAPI do Outlook. Clique com o botão direito do mouse na pasta zip do número de versão do **OutlookMAPISamples \< \>** e clique em **Extrair Tudo.**
    
3. Clique **em** Procurar, selecione o local onde deseja salvar o exemplo e clique em **Extrair.**
    
4. Execute o Visual Studio 2008.
    
5. No Visual Studio 2008, clique em **Arquivo,** selecione **Abrir** e clique em **Projeto/Solução.**
    
6. Navegue até o local onde você salvou o exemplo, clique em **mrxp32.vcproj** e clique em **Abrir**.
    
7. No menu **Criar,** clique em **Configuration Manager.**
    
8. Na caixa de **diálogo Configuration Manager,** vá para a linha  **mrxp32** e, na coluna Configuração, selecione **Liberar** e clique em **Fechar.**
    
9. On the **Build** menu, click **Build Solution**.
    
10. Na caixa **de diálogo Salvar Arquivo como,** clique em **Salvar.**
    
11. Na pasta onde você salvou o exemplo, clique com o botão direito do mouse no arquivo de lote de instalação e clique em **Executar como administrador.**
    
12. Na caixa de diálogo **Controle de Conta de Usuário**, clique em **Continuar**.
    
    > [!NOTE]
    > **install.bat** copia a .dll para a pasta de instalação padrão do Microsoft Office, C:\Arquivos de Programas\Microsoft Office\Office12\. Se você instalou produtos do Office em um local diferente, clique com o botão direito do mouse **install.bat** e clique em **Editar.** O arquivo é aberto no Bloco de Notas. Substitua o caminho de instalação padrão pelo caminho de instalação usado no computador. 
  
 **Para configurar o Provedor de Transporte no Outlook**
  
1. No menu **Ferramentas** do Outlook, clique em **Configurações da Conta.**
    
2. Na caixa **de diálogo Configurações da** Conta, na guia **Email,** clique em **Novo.**
    
3. Em **Choose Email Service** click **Other**, select **MRXP Sample Transport**, and then click **Next**.
    
4. Na caixa de diálogo Configuração de **Transporte MRXP,** digite um **Nome de Exibição do Usuário.**
    
5. Em **Caminho para Caixa de Entrada (Compartilhamento UNC),** insira um caminho de pasta. Isso também pode ser um caminho para uma pasta local. 
    
    > [!IMPORTANT]
    > Esse caminho deve existir. 
  
6. Clique em **OK**.
    
7. Na caixa **de diálogo Adicionar Conta de Email,** clique em **OK.** Clique **em Concluir** e em **Fechar.**
    
8. Para começar a usar a conta MRXP, saia e reinicie o Outlook.
    
 **Para usar o exemplo de provedor de transporte para enviar uma mensagem no Outlook**
  
1. No menu **Arquivo,** clique em **Novo** e em Mensagem **de Email.**
    
2. Na caixa **Para,** digite o nome do destinatário usando o **formato [MRXP: \< ENDEREÇO \> ]**. O endereço é o compartilhamento UNC ou o caminho da pasta local para a caixa de entrada do destinatário.
    
    > [!NOTE]
    > Se houver dois-pontos ou uma malha invertida no endereço, você deve inserir uma faixa invertida antes de cada dois-pontos ou uma faixa invertida. Por exemplo, para enviar emails para [MRXP:C:\Mail\myDir] você deve digitar  `[MRXP:C\:\\Mail\\myDir]` . 
  
    > [!IMPORTANT]
    > O endereço do destinatário deve existir. 
  
3. Clique **em Conta** e em Transporte de Exemplo **MRXP.**
    
4. Digite sua mensagem e clique em **Enviar**. A mensagem é enviada usando o provedor de transporte MRXP.
    
 **Para usar o exemplo de provedor de transporte para receber uma mensagem no Outlook**
  
1. No menu **Arquivo,** clique em **Novo** e em Mensagem **de Email.**
    
2. Digite sua mensagem.
    
3. Clique no **Botão do Microsoft Office,**  clique em Salvar **como** e, em seguida, clique em Salvar como para salvar o arquivo na pasta da caixa de entrada especificada durante a instalação. 
    
4. Na caixa **de diálogo Salvar como,** navegue até o compartilhamento UNC ou pasta local que você definiu como sua caixa de entrada. 
    
5. No drop **down Salvar como tipo,** clique em **Formato de Mensagem do Outlook.**
    
6. Digite um nome para o arquivo e clique em **Salvar.**
    
7. O arquivo é salvo na pasta compartilhada. O provedor de transporte MRXP entrega a mensagem à sua Caixa de Entrada no Outlook.
    

