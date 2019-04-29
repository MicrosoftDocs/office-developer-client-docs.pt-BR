---
title: Adicionar um manipulador de eventos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- evento versionupgrade [InfoPath 2007], tratamento de eventos [InfoPath 2007], alteração de evento [InfoPath 2007], InfoPath 2007, adição de manipuladores de eventos, evento Changed [InfoPath 2007], Evento ContextChanged [InfoPath 2007], eventos [InfoPath 2007], eventos [InfoPath 2007], adicionando manipuladores de eventos, evento assinar [InfoPath 2007], evento ViewSwitched [InfoPath 2007], tratamento de eventos [InfoPath 2007], evento Merge [InfoPath 2007], evento Validating [InfoPath 2007], enviar evento [InfoPath 2007], salvar evento [InfoPath 2007], carregando evento [InfoPath 2007]
localization_priority: Normal
ms.assetid: d69393fb-fb5a-4edb-abc0-38f5d7e80bcc
description: Este tópico descreve os procedimentos para adicionar manipuladores de eventos a um modelo de formulário de código gerenciado do Microsoft InfoPath usando o Visual Studio 2012. Para adicionar um manipulador de eventos a um modelo de formulário, inicie com o modelo de formulário aberto no designer do InfoPath e, em seguida, selecione o comando de interface do usuário apropriado para o evento para o qual você deseja escrever o código. Depois de selecionar o comando para um evento no designer do InfoPath, o foco mudará automaticamente para o manipulador de eventos esqueleto desse evento no editor de código do Visual Studio 2012.
ms.openlocfilehash: c6406ec1604355c59f4ee4818fdaea5d70f696bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427182"
---
# <a name="add-an-event-handler"></a>Adicionar um manipulador de eventos

Este tópico descreve os procedimentos para adicionar manipuladores de eventos a um modelo de formulário de código gerenciado do Microsoft InfoPath usando o Visual Studio 2012. Para adicionar um manipulador de eventos a um modelo de formulário, inicie com o modelo de formulário aberto no designer do InfoPath e, em seguida, selecione o comando de interface do usuário apropriado para o evento para o qual você deseja escrever o código. Depois de selecionar o comando para um evento no designer do InfoPath, o foco mudará automaticamente para o manipulador de eventos esqueleto desse evento no editor de código do Visual Studio 2012.
  
> [!IMPORTANT]
> Você deve sempre usar a interface de usuário do InfoPath designer para adicionar um manipulador de eventos. Adicionar um manipulador de eventos com a interface de usuário gera o código de associação de eventos no método **InternalStartup** do arquivo FormCode.cs ou FormCode. vb no seu projeto de modelo de formulário. Você não deve criar o método **InternalStartup** ou adicionar qualquer código adicional nele mesmo. 
  
### <a name="add-an-event-handler-for-the-click-event-of-a-button-control"></a>Adicionar um manipulador de eventos para o evento Click de um controle Button

1. Abra o modelo de formulário no designer do InfoPath e, em seguida, adicione um controle de **botão** ao formulário. 
    
2. Clique no botão e, na guia **Propriedades** da faixa de opções, clique em **código personalizado**.
    
    O foco alterna para o manipulador de eventos esqueleto do [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) evento clicado no editor de código do Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-changing-validating-or-changed-event-of-a-field-or-group"></a>Adicionar um manipulador de eventos para o evento Changing, Validating ou Changed de um campo ou grupo

1. Abra o modelo de formulário no designer do InfoPath.
    
2. Clique com o botão direito do mouse em um controle de inserção de dados associado ao campo ou grupo, como um controle **Caixa de Texto**. 
    
3. Aponte para **programação**e, em seguida, clique no evento para o qual você deseja criar um manipulador de eventos. O foco alterna para o manipulador de eventos esqueleto para o evento [Changing](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) , [Validating](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) ou [Changed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) no editor de código do Visual Studio 2012. 
    
    > [!NOTE]
    > O comando para criar um manipulador de eventos para o evento **Changing** não estará disponível se a configuração de compatibilidade do modelo de formulário estiver definida como **formulário de navegador da Web**. Isso ocorre porque o evento **Changing** não é suportado na lógica de negócios dos modelos de formulário publicados em bibliotecas de documentos no Microsoft SharePoint Server 2010 com o InfoPath Forms Services. Para criar um manipulador de eventos para o evento **Changing** , você deve alterar a configuração de compatibilidade para o **Editor do InfoPath** no designer do InfoPath. Para fazer isso, clique na guia **arquivo** , em **Opções de formulário**, em **compatibilidade**e, em seguida, defina tipo de **formulário** como formulário do **Editor do InfoPath**. 
  
### <a name="add-an-event-handler-for-the-loading-viewswitched-contextchanged-and-sign-events-of-a-form"></a>Adicionar um manipulador de eventos para os eventos loading, ViewSwitched, ContextChanged e Sign de um formulário

1. Abra o modelo de formulário no designer do InfoPath.
    
2. Na guia **desenvolvedor** da faixa de opções, clique no evento de formulário para o qual você deseja gravar um manipulador de eventos. 
    
    O foco alterna para o manipulador de eventos esqueleto para o evento [loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) , [ViewSwitched](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) , ContextChanged ou [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) no editor de código do Visual Studio 2012. [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) 
    
    > [!NOTE]
    > Os comandos para criar um manipulador de eventos para [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) os eventos ContextChanged ou [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) não estarão disponíveis se a configuração de compatibilidade do modelo de formulário estiver definida como **formulário de navegador da Web**. Isso ocorre porque não há suporte para esses eventos na lógica de negócios dos modelos de formulário publicados em bibliotecas de documentos no Microsoft SharePoint Server 2010 com o InfoPath Forms Services. Para criar um manipulador de eventos para [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) o evento ContextChanged ou [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) , você deve alterar o formulário configuração de compatibilidade para o **Editor do InfoPath** no designer do InfoPath. Para fazer isso, clique na guia **arquivo** , em **Opções de formulário**, em **compatibilidade**e, em seguida, defina tipo de **formulário** como formulário do **Editor do InfoPath**. 
  
### <a name="add-an-event-handler-for-the-submit-event-of-a-form"></a>Adicionar um manipulador de eventos para o evento Submit de um formulário

1. Abra o modelo de formulário no designer do InfoPath.
    
2. Clique na guia **arquivo** , clique em **Enviar para** na guia **informações** e, em seguida, clique em * * opções de envio * *.
    
3. Clique em **permitir que os usuários enviem este formulário**, clique em **executar ação personalizada usando código**e, em seguida, clique em **Editar código**.
    
    O foco alterna para o manipulador de eventos esqueleto para o evento de [envio](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) no editor de código do Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-save-event-of-a-form"></a>Adicionar um manipulador de eventos para o evento Save de um formulário

1. Abra o modelo de formulário no designer do InfoPath.
    
2. Clique na guia **Arquivo** e em **Opções de Formulário**. Depois, clique na guia **Informações**. 
    
3. Clique na categoria **salvar** , marque a caixa de seleção **salvar usando código personalizado** e clique em **Editar**.
    
    O foco alterna para o manipulador de eventos esqueleto do evento [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) no editor de código do Visual Studio 2012. 
    
    > [!NOTE]
    > A caixa de seleção **salvar usando código personalizado** não estará disponível se a configuração de compatibilidade do modelo de formulário estiver definida como **InfoPath Forms Services**. Isso ocorre porque o evento [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) não é suportado na lógica de negócios dos modelos de formulário publicados em bibliotecas de documentos no Microsoft SharePoint Server 2010 com o InfoPath Forms Services. Para criar um manipulador de eventos para o evento [salvar](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) , você deve alterar a configuração de compatibilidade para o **formulário do editor do InfoPath** no designer do InfoPath. Para fazer isso, clique na guia **arquivo** , em **Opções de formulário**, em **compatibilidade**e, em seguida, defina tipo de **formulário** como formulário do **Editor do InfoPath**. 
  
### <a name="add-an-event-handler-for-the-versionupgrade-event-of-a-form"></a>Adicionar um manipulador de eventos para o evento VersionUpgrade de um formulário

1. Abra o modelo de formulário no designer do InfoPath.
    
2. Clique na guia **Arquivo** e em **Opções de Formulário**. Depois, clique na guia **Informações**. 
    
3. Clique na **categoria controle de versão** , selecione **usar evento personalizado** na caixa suspensa **atualizar formulários existentes** e, em seguida, clique em **Editar**.
    
    O foco alterna para o manipulador de eventos esqueleto do evento [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) no editor de código do Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-merge-event-of-a-form"></a>Adicionar um manipulador de eventos para o evento Merge de um formulário

1. Abra o modelo de formulário no designer do InfoPath.
    
2. Clique na guia **Arquivo** e em **Opções de Formulário**. Depois, clique na guia **Informações**. 
    
3. Clique na categoria **avançado** , clique na caixa de seleção **habilitar mesclagem de formulários** , clique na caixa de seleção mesclar **usando código personalizado** e, em seguida, clique em **Editar**.
    
    O foco alterna para o manipulador de eventos esqueleto para o evento [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) no editor de código do Visual Studio 2012. 
    
    > [!NOTE]
    > A caixa de seleção **habilitar mesclagem de formulários** não estará disponível se a configuração de compatibilidade do modelo de formulário estiver definida como **InfoPath Forms Services**. Isso ocorre porque não há suporte para o evento [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) na lógica de negócios dos modelos de formulário publicados em bibliotecas de documentos no Microsoft SharePoint Server 2010 com o InfoPath Forms Services. Para criar um manipulador de eventos para o evento [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) , você deve alterar a configuração de compatibilidade para o **formulário do editor do InfoPath** no designer do InfoPath. Para fazer isso, clique na guia **arquivo** , em **Opções de formulário**, em **compatibilidade**e, em seguida, defina tipo de **formulário** como formulário do **Editor do InfoPath**. 
  
## <a name="see-also"></a>Confira também



[Passo a passo: Criando um modelo de formulário básico com código](walkthrough-creating-a-basic-form-template-with-code.md)

