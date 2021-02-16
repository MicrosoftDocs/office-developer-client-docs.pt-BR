---
title: MFCMAPI como exemplo de código
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f98eb842-fe76-4f60-b5e2-d2217d1a66ad
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d72c224db8b3ae4bb6fee3d34f73d9949cda6b8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356858"
---
# <a name="mfcmapi-as-a-code-sample"></a>MFCMAPI como exemplo de código
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O exemplo MFCMAPI usa a API de Mensagens para fornecer acesso a armazenamentos MAPI por meio de uma interface gráfica do usuário. Depois de baixar esse exemplo, você pode usar os arquivos de origem para examinar exemplos de casos de uso de muitas das interfaces e referências MAPI. Para obter mais informações, consulte [Interfaces MAPI](mapi-interfaces.md).
  
|||
|:-----|:-----|
|Plataformas:  <br/> |Microsoft Visual Studio 2008 para compilar para Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2 e Windows Server 2003 SP1  <br/> |
   
### <a name="to-download-mfcmapi"></a>Para baixar MFCMAPI
  
1. Na página [MFCMAPI,](https://codeplex.com/MFCMAPI) clique na guia **Código-fonte.** 
    
2. Em **Check-Ins Recentes,** clique **em Baixar** para a com build mais recente. 
    
3. Leia o contrato de licença e clique em **Concordar.**
    
4. Na caixa de diálogo **Download de Arquivo**, clique em **Salvar**. Na caixa **de diálogo Salvar como,** localize a pasta na qual você deseja salvar os arquivos de origem e clique em **Salvar.**
    
5. Na caixa **de diálogo Baixar Concluído,** clique em **Abrir Pasta.** Você também pode clicar **em Fechar** para fechar a caixa de diálogo e localizar os arquivos de origem recortados na pasta em que os salvou. 
    
6. Clique com o botão direito do mouse no arquivo .zip do número de versão **\< \> MFCMAPI** e clique em **Extrair Tudo.** Na caixa de diálogo exibida, clique em **Extrair** para extrair os arquivos para a pasta exibida. Você também pode clicar **em Procurar** para selecionar ou criar uma pasta diferente. 
    
7. Execute o Visual Studio 2008 como administrador.
    
   > [!NOTE]
   > Se o computador estiver executando o Windows XP, você deverá estar conectado como administrador. Se o computador estiver executando o Windows Vista, você deverá estar conectado como administrador e clicar com o botão direito do mouse no ícone do Visual Studio 2008 e clicar em Executar **como administrador.** 
  
8. No Visual Studio 2008, clique em **Arquivo,** aponte para **Abrir** e clique em **Projeto/Solução.**
    
9. Navegue até o local onde você salvou o exemplo, selecione **MFCMapi.vcproj** e clique em **Abrir**.
    
10. On the **Build** menu, click **Build Solution**.
    
11. Na caixa **de diálogo Salvar Arquivo como,** clique em **Salvar.**
    
### <a name="to-use-mfcmapi-as-a-code-sample"></a>Para usar MFCMAPI como um exemplo de código
  
No **Solution Explorer,** expanda o projeto **MFCMapi** e examine os arquivos nos nós Arquivos de **Header**, **Arquivos** de Recurso e Arquivos **de** Origem para cenários de programação. 
  
Muitos tópicos de método na seção [Interfaces MAPI](mapi-interfaces.md) apontam para arquivos de origem MFCMAPI para exemplos de programação. Por exemplo, em [IMsgStore::GetReceiveFolderTable,](imsgstore-getreceivefoldertable.md) você é instruído a olhar para a função no  `CMsgStoreDlg::OnDisplayReceiveFolderTable` arquivo MsgStoreDlg.cpp. 
  
## <a name="see-also"></a>Confira também

- [Amostras MAPI](mapi-samples.md)

