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
  
O exemplo MFCMAPI usa a API de mensagens para fornecer acesso a repositórios MAPI por meio de uma interface gráfica do usuário. Depois de baixar esse exemplo, você pode usar os arquivos de origem para examinar exemplos de uso de exemplo para muitas das referências e interfaces MAPI. Para obter mais informações, consulte [interfaces MAPI](mapi-interfaces.md).
  
|||
|:-----|:-----|
|Plataformas  <br/> |Microsoft Visual Studio 2008 para compilar para Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2 e Windows Server 2003 SP1  <br/> |
   
### <a name="to-download-mfcmapi"></a>Para baixar o MFCMAPI
  
1. Na página [MFCMAPI](https://codeplex.com/MFCMAPI) , clique na guia **código-fonte** . 
    
2. Em **check-ins recentes**, clique em **baixar** para a compilação mais recente. 
    
3. Leia o contrato de licença e clique em **concordo**.
    
4. Na caixa de diálogo **Download de Arquivo**, clique em **Salvar**. Na caixa de diálogo **salvar como** , localize a pasta na qual você deseja salvar os arquivos de origem e clique em **salvar**.
    
5. Na caixa de diálogo **baixar completo** , clique em **abrir pasta**. Você também pode clicar em **fechar** para fechar a caixa de diálogo e localizar os arquivos de origem compactados na pasta em que foram salvos. 
    
6. Clique com o botão direito do mouse no arquivo **MFCMAPI-\<version number\>. zip** e clique em **extrair tudo**. Na caixa de diálogo exibida, clique em **extrair** para extrair os arquivos para a pasta exibida. Você também pode clicar em **procurar** para selecionar ou criar uma pasta diferente. 
    
7. Execute o Visual Studio 2008 como um administrador.
    
   > [!NOTE]
   > Se o computador estiver executando o Windows XP, você deverá estar conectado como administrador. Se seu computador está executando o Windows Vista, você deve estar conectado como administrador e deve clicar com o botão direito do mouse no ícone do Visual Studio 2008 e, em seguida, clique em **Executar como administrador**. 
  
8. No Visual Studio 2008, clique em **arquivo**, aponte para **abrir**e, em seguida, clique em **projeto/solução**.
    
9. Navegue até o local onde você salvou o exemplo, selecione **MFCMapi. vcproj**e clique em **abrir**.
    
10. On the **Build** menu, click **Build Solution**.
    
11. Na caixa de diálogo **salvar arquivo como** , clique em **salvar**.
    
### <a name="to-use-mfcmapi-as-a-code-sample"></a>Para usar o MFCMAPI como um exemplo de código
  
No **Gerenciador de soluções**, expanda o projeto **MFCMapi** e examine os arquivos nos nós **arquivos de cabeçalho**, **arquivos de recurso**e **arquivos de origem** para cenários de programação. 
  
Muitos tópicos de método na seção [interfaces MAPI](mapi-interfaces.md) apontam para os arquivos de origem do MFCMAPI para exemplos de programação. Por exemplo, em [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) você é instruído a examinar a função `CMsgStoreDlg::OnDisplayReceiveFolderTable` no arquivo MsgStoreDlg. cpp. 
  
## <a name="see-also"></a>Confira também

- [Amostras MAPI (em inglês)](mapi-samples.md)

