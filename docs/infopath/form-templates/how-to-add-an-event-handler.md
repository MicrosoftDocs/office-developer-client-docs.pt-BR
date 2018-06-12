---
title: Adicionar um manipulador de eventos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- evento versionupgrade [infopath 2007], manipulação de eventos [InfoPath 2007], alterando o evento [InfoPath 2007], InfoPath 2007, adicionando manipuladores de eventos, evento Changed [InfoPath 2007], evento ContextChanged [InfoPath 2007], clique em evento [InfoPath 2007], [InfoPath de eventos Carregando enviar evento [InfoPath 2007], salvar evento [InfoPath 2007], 2007], adicionando manipuladores de eventos, o evento de entrada [InfoPath 2007], evento ViewSwitched [InfoPath 2007], [InfoPath 2007] de manipulação de eventos, evento direta [InfoPath 2007], o evento Validando [InfoPath 2007] evento [InfoPath 2007]
localization_priority: Normal
ms.assetid: d69393fb-fb5a-4edb-abc0-38f5d7e80bcc
description: Este tópico descreve os procedimentos para adicionar manipuladores de eventos para um modelo de formulário do Microsoft InfoPath código gerenciado usando o Visual Studio 2012. Para adicionar um manipulador de eventos para um modelo de formulário, iniciar com o modelo de formulário aberto no InfoPath Designer e, em seguida, selecione o comando de interface de usuário apropriados para o evento que deseja gravar código para. Depois de selecionar o comando para um evento no InfoPath Designer, o foco alterna automaticamente para o manipulador de eventos reduzida para o evento no editor de código do Visual Studio 2012.
ms.openlocfilehash: 5bac409fb859337b82bf6567dd4636e6d384ba59
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765640"
---
# <a name="add-an-event-handler"></a>Adicionar um manipulador de eventos

Este tópico descreve os procedimentos para adicionar manipuladores de eventos para um modelo de formulário do Microsoft InfoPath código gerenciado usando o Visual Studio 2012. Para adicionar um manipulador de eventos para um modelo de formulário, iniciar com o modelo de formulário aberto no InfoPath Designer e, em seguida, selecione o comando de interface de usuário apropriados para o evento que deseja gravar código para. Depois de selecionar o comando para um evento no InfoPath Designer, o foco alterna automaticamente para o manipulador de eventos reduzida para o evento no editor de código do Visual Studio 2012.
  
> [!IMPORTANT]
> Você sempre deve usar a interface de usuário do InfoPath Designer para adicionar um manipulador de eventos. Adicionar um manipulador de eventos com a interface do usuário gera um código de ligação de evento no método **InternalStartup** do arquivo FormCode.cs ou FormCode.vb em seu projeto de modelo de formulário. Você não deve criar o método **InternalStartup** ou adicione qualquer código adicional dentro da mesmo. 
  
### <a name="add-an-event-handler-for-the-click-event-of-a-button-control"></a>Adicionar um manipulador de eventos para o evento Click de um controle de botão

1. Abra o modelo de formulário no InfoPath Designer e, em seguida, adicionar um controle de **botão** ao formulário. 
    
2. Clique no botão e, em seguida, na guia **Propriedades** da faixa de opções, clique em **Código personalizado**.
    
    O foco alterna para o manipulador de eventos reduzida para o evento [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) no editor de código do Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-changing-validating-or-changed-event-of-a-field-or-group"></a>Adicionar um manipulador de eventos para o evento Changing, validando ou alterado do campo ou grupo

1. Abra o modelo de formulário no Designer do InfoPath.
    
2. Clique com o botão um controle de entrada de dados vinculado ao campo ou grupo, como um controle de **Caixa de texto** . 
    
3. Aponte para **programação**e, em seguida, clique no evento que você deseja criar um manipulador de eventos. O foco alterna para o manipulador de eventos reduzida para o evento [Changing](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) , [Validando](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) ou [alterado](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) no editor de código do Visual Studio 2012. 
    
    > [!NOTE]
    > O comando para criar um manipulador de eventos para o evento **Changing** não estará disponível se a configuração de compatibilidade do modelo de formulário está definida como **Formulário de navegador da Web**. Isso acontece porque não há suporte para o evento **Changing** na lógica de negócios de modelos de formulário publicados em bibliotecas de documentos no Microsoft SharePoint Server 2010 com o InfoPath Forms Services. Para criar um manipulador de eventos para o evento **Changing** , você deve alterar a configuração de compatibilidade para o **InfoPath Editor** no designer do InfoPath. Para fazer isso, clique na guia **arquivo** , clique em **Opções de formulário**, clique em **compatibilidade**e, em seguida, defina o **tipo de formulário** como o **Formulário do InfoPath Editor**. 
  
### <a name="add-an-event-handler-for-the-loading-viewswitched-contextchanged-and-sign-events-of-a-form"></a>Adicionar um manipulador de eventos para os eventos de entrada, ViewSwitched, ContextChanged e carregamento de um formulário

1. Abra o modelo de formulário no Designer do InfoPath.
    
2. Na guia **desenvolvedor** da faixa de opções, clique no evento de formulário que você deseja gravar um manipulador de eventos. 
    
    O foco alterna para o manipulador de eventos reduzida para o evento de [carregamento](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) , [ViewSwitched](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) , [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) ou uma [entrada](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) no editor de código do Visual Studio 2012. 
    
    > [!NOTE]
    > Os comandos para criar um manipulador de eventos para os eventos [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) ou [entrada](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) não estarão disponíveis se a configuração de compatibilidade do modelo de formulário está definida como **Formulário de navegador da Web**. Isso ocorre porque esses eventos não são suportados na lógica de negócios de modelos de formulário publicados em bibliotecas de documentos no Microsoft SharePoint Server 2010 com o InfoPath Forms Services. Para criar um manipulador de eventos para o evento [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) ou [entrar](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) , você deve alterar a configuração de compatibilidade para o **Formulário do InfoPath Editor** no InfoPath Designer. Para fazer isso, clique na guia **arquivo** , clique em **Opções de formulário**, clique em **compatibilidade**e, em seguida, defina o **tipo de formulário** como o **Formulário do InfoPath Editor**. 
  
### <a name="add-an-event-handler-for-the-submit-event-of-a-form"></a>Adicionar um manipulador de eventos para o evento de envio de um formulário

1. Abra o modelo de formulário no Designer do InfoPath.
    
2. Clique na guia **arquivo** , clique em **Enviar para** , na guia **informações** e, em seguida, clique em * * Opções de envio * *.
    
3. Clique em **Permitir que os usuários enviem este formulário**, clique em **Executar ação personalizada usando o código**e, em seguida, clique em **Editar código**.
    
    O foco alterna para o manipulador de eventos reduzida para o evento de [envio](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) no editor de código do Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-save-event-of-a-form"></a>Adicionar um manipulador de eventos para o evento de salvamento de um formulário

1. Abra o modelo de formulário no Designer do InfoPath.
    
2. Clique na guia **arquivo** e clique em **Opções de formulário** , na guia **informações** . 
    
3. Clique na categoria **Salvar** , marque a caixa de seleção **Salvar usando código personalizado** e, em seguida, clique em **Editar**.
    
    O foco alterna para o manipulador de eventos reduzida para o evento [Salvar](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) no editor de código do Visual Studio 2012. 
    
    > [!NOTE]
    > A caixa de seleção **Salvar usando código personalizado** não está disponível se a configuração de compatibilidade do modelo de formulário estiver definida como o **InfoPath Forms Services**. Isso acontece porque não há suporte para o evento de [Salvar](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) na lógica de negócios de modelos de formulário publicados em bibliotecas de documentos no Microsoft SharePoint Server 2010 com o InfoPath Forms Services. Para criar um manipulador de eventos para o evento de [Salvar](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) , você deve alterar a configuração de compatibilidade para o **Formulário do InfoPath Editor** no InfoPath Designer. Para fazer isso, clique na guia **arquivo** , clique em **Opções de formulário**, clique em **compatibilidade**e, em seguida, defina o **tipo de formulário** como o **Formulário do InfoPath Editor**. 
  
### <a name="add-an-event-handler-for-the-versionupgrade-event-of-a-form"></a>Adicionar um manipulador de eventos para o evento VersionUpgrade de um formulário

1. Abra o modelo de formulário no Designer do InfoPath.
    
2. Clique na guia **arquivo** e clique em **Opções de formulário** , na guia **informações** . 
    
3. Clique na categoria de **controle de versão** , selecione o **evento de uso personalizado** na caixa suspensa **Atualizar formulários existentes** e, em seguida, clique em **Editar**.
    
    O foco alterna para o manipulador de eventos reduzida para o evento [Salvar](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) no editor de código do Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-merge-event-of-a-form"></a>Adicionar um manipulador de eventos para o evento de mesclagem de um formulário

1. Abra o modelo de formulário no Designer do InfoPath.
    
2. Clique na guia **arquivo** e clique em **Opções de formulário** , na guia **informações** . 
    
3. Clique na categoria **Avançado** , clique na caixa de seleção **Habilitar mesclagem de formulários** , clique na caixa de seleção **Mesclar usando código personalizado** e, em seguida, clique em **Editar**.
    
    O foco alterna para o manipulador de eventos reduzida para o evento [Mesclar](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) no editor de código do Visual Studio 2012. 
    
    > [!NOTE]
    > A caixa de seleção **Habilitar mesclagem de formulários** não estará disponível se a configuração de compatibilidade do modelo de formulário está definida para o **InfoPath Forms Services**. Isso acontece porque não há suporte para o evento [Mesclar](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) na lógica de negócios de modelos de formulário publicados em bibliotecas de documentos no Microsoft SharePoint Server 2010 com o InfoPath Forms Services. Para criar um manipulador de eventos para o evento [Mesclar](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) , você deve alterar a configuração de compatibilidade para o **Formulário do InfoPath Editor** no InfoPath Designer. Para fazer isso, clique na guia **arquivo** , clique em **Opções de formulário**, clique em **compatibilidade**e, em seguida, defina o **tipo de formulário** como o **Formulário do InfoPath Editor**. 
  
## <a name="see-also"></a>Confira também



[Passo a passo: Criando um modelo de formulário básico com código](walkthrough-creating-a-basic-form-template-with-code.md)

