---
title: MFCMAPI como um exemplo de código
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f98eb842-fe76-4f60-b5e2-d2217d1a66ad
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b4d46dc8a84b52605d09a694e6873cb3813ae5b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578112"
---
# <a name="mfcmapi-as-a-code-sample"></a>MFCMAPI como um exemplo de código
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O exemplo MFCMAPI usa a API do serviço de mensagens para fornecer acesso a repositórios MAPI através de uma interface gráfica do usuário. Após você baixa esse exemplo, você pode usar os arquivos de origem para examinar os casos de uso de exemplo para muitas das interfaces MAPI e referências. Para obter mais informações, consulte [Interfaces de MAPI](mapi-interfaces.md).
  
|||
|:-----|:-----|
|Plataformas:  <br/> |Microsoft Visual Studio 2008 para compilar para Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2 e Windows Server 2003 SP1  <br/> |
   
### <a name="to-download-mfcmapi"></a>Para baixar MFCMAPI
  
1. Na página [MFCMAPI](http://codeplex.com/MFCMAPI) , clique na guia do **Código-fonte** . 
    
2. Em **Recentes Check-Ins**, clique em **Download** para a compilação mais recente. 
    
3. Leia o contrato de licença e clique em **concordo**.
    
4. Na caixa de diálogo **Download de arquivo** , clique em **Salvar**. Na caixa de diálogo **Salvar como** , localize a pasta na qual deseja salvar os arquivos de origem e, em seguida, clique em **Salvar**.
    
5. Na caixa de diálogo **Download concluído** , clique em **Abrir pasta**. Também é possível clicar **Fechar** para fechar a caixa de diálogo e localize os arquivos de origem compactados na pasta que você salvou-los na. 
    
6. Com o botão direito do **MFCMAPI -\<número da versão\>. zip** de arquivo e clique em **Extrair todos**. Na caixa de diálogo que aparece, clique em **extrair** para extrair os arquivos para a pasta que é exibida. Você também pode clicar em **Procurar** para selecionar ou criar uma pasta diferente. 
    
7. Execute o Visual Studio 2008 como administrador.
    
   > [!NOTE]
   > Se seu computador estiver executando o Windows XP, você deve ser logado como administrador. Se seu computador estiver executando o Windows Vista, você deve estar logado como administrador e você deve com o botão direito no ícone do Visual Studio 2008 e clique em **Executar como administrador**. 
  
8. No Visual Studio 2008, clique em **arquivo**, aponte para **Abrir**e, em seguida, clique em **Project/Solution**.
    
9. Navegue até o local onde você salvou a amostra, selecione **MFCMapi.vcproj**e clique em **Abrir**.
    
10. On the **Build** menu, click **Build Solution**.
    
11. Na caixa de diálogo **Salvar arquivo como** , clique em **Salvar**.
    
### <a name="to-use-mfcmapi-as-a-code-sample"></a>Para usar MFCMAPI como um exemplo de código
  
No **Solution Explorer**, expanda o projeto **MFCMapi** e examinar os arquivos nos nós de **Arquivos de cabeçalho**, **Arquivos de recursos**e **Arquivos de origem** para cenários de programação. 
  
Muitos tópicos do método na seção de [Interfaces de MAPI](mapi-interfaces.md) apontam para os arquivos de origem MFCMAPI para obter exemplos de programação. Por exemplo, no [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) instruído para examinar a função `CMsgStoreDlg::OnDisplayReceiveFolderTable` no arquivo MsgStoreDlg.cpp. 
  
## <a name="see-also"></a>Confira também

- [Amostras MAPI](mapi-samples.md)

