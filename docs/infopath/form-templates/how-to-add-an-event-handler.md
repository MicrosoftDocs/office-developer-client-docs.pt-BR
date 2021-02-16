---
title: Adicionar um manipulador de eventos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- evento versionupgrade [infopath 2007], manipulação de eventos [InfoPath 2007],Evento Changing [InfoPath 2007],InfoPath 2007, adicionando manipuladores de eventos,Evento Alterado [InfoPath 2007],evento ContextChanged [InfoPath 2007],Evento Click [InfoPath 2007],eventos [InfoPath 2007], adicionando manipuladores de eventos, evento Sign [InfoPath 2007], evento ViewSwitched [InfoPath 2007],manipulação de eventos [InfoPath 2007], evento Merge [InfoPath 2007],Evento de validação [InfoPath 2007],Evento Enviar [InfoPath 2007],Evento Save [InfoPath 2007] ,Evento Loading [InfoPath 2007]
localization_priority: Normal
ms.assetid: d69393fb-fb5a-4edb-abc0-38f5d7e80bcc
description: Este tópico descreve os procedimentos para adicionar manipuladores de eventos a um modelo de formulário de código gerenciado do Microsoft InfoPath usando o Visual Studio 2012. Para adicionar um manipulador de eventos a um modelo de formulário, comece com o modelo de formulário aberto no InfoPath Designer e, em seguida, selecione o comando de interface de usuário apropriado para o evento para o que você deseja escrever código. Depois de selecionar o comando para um evento no InfoPath Designer, o foco alterna automaticamente para o manipulador de eventos esqueleto desse evento no editor de código do Visual Studio 2012.
ms.openlocfilehash: c6406ec1604355c59f4ee4818fdaea5d70f696bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427182"
---
# <a name="add-an-event-handler"></a>Adicionar um manipulador de eventos

Este tópico descreve os procedimentos para adicionar manipuladores de eventos a um modelo de formulário de código gerenciado do Microsoft InfoPath usando o Visual Studio 2012. Para adicionar um manipulador de eventos a um modelo de formulário, comece com o modelo de formulário aberto no InfoPath Designer e, em seguida, selecione o comando de interface de usuário apropriado para o evento para o que você deseja escrever código. Depois de selecionar o comando para um evento no InfoPath Designer, o foco alterna automaticamente para o manipulador de eventos esqueleto desse evento no editor de código do Visual Studio 2012.
  
> [!IMPORTANT]
> Você sempre deve usar a interface do usuário do InfoPath Designer para adicionar um manipulador de eventos. A adição de um manipulador de eventos com a interface do usuário gera código de associação de eventos no método **InternalStartup** do arquivo FormCode.cs ou FormCode.vb no projeto do modelo de formulário. Você não deve criar o **método InternalStartup** nem adicionar qualquer código adicional nele por conta própria. 
  
### <a name="add-an-event-handler-for-the-click-event-of-a-button-control"></a>Adicionar um manipulador de eventos para o evento Click de um controle Button

1. Abra o modelo de formulário no InfoPath Designer e adicione um controle **Button** ao formulário. 
    
2. Clique no botão e, na guia **Propriedades** da faixa de opções, clique em **Código Personalizado.**
    
    O foco alterna para o manipulador de eventos esqueleto [do evento Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) no editor de código do Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-changing-validating-or-changed-event-of-a-field-or-group"></a>Adicionar um manipulador de eventos para o evento Changing, Validating ou Changed de um campo ou grupo

1. Abra o modelo de formulário no InfoPath Designer.
    
2. Clique com o botão direito do mouse em um controle de inserção de dados associado ao campo ou grupo, como um controle **Caixa de Texto**. 
    
3. Aponte para **Programação** e clique no evento para o que você deseja criar um manipulador de eventos. O foco alterna para o manipulador de eventos esqueleto para o evento [Changing](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) , [Validating](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) ou [Changed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) no editor de código do Visual Studio 2012. 
    
    > [!NOTE]
    > O comando para criar um manipulador de eventos para o evento **Changing** não estará disponível se a configuração de compatibilidade do modelo de formulário estiver definida como Formulário **do Navegador da Web.** Isso ocorre porque o evento **Changing** não tem suporte na lógica de negócios de modelos de formulário publicados em bibliotecas de documentos no Microsoft SharePoint Server 2010 com o InfoPath Forms Services. Para criar um manipulador de eventos para o evento **Changing,** você deve alterar a configuração de compatibilidade para o Editor do **InfoPath** no designer do InfoPath. Para fazer isso, clique **na** guia Arquivo, clique em  Opções de **Formulário,** clique em Compatibilidade **e,** em seguida, de definir o tipo de formulário para o Formulário do Editor **do InfoPath.** 
  
### <a name="add-an-event-handler-for-the-loading-viewswitched-contextchanged-and-sign-events-of-a-form"></a>Adicionar um manipulador de eventos para os eventos Loading, ViewSwitched, ContextChanged e Sign de um formulário

1. Abra o modelo de formulário no InfoPath Designer.
    
2. Na guia **Desenvolvedor da** faixa de opções, clique no evento de formulário para o que você deseja gravar um manipulador de eventos. 
    
    O foco alterna para o manipulador de eventos esqueleto para [o evento Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) , [ViewSwitched](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) , [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) ou [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) no editor de código do Visual Studio 2012. 
    
    > [!NOTE]
    > Os comandos para criar um manipulador de eventos para os eventos [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) ou [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) não estarão disponíveis se a configuração de compatibilidade do modelo de formulário estiver definida como Formulário do Navegador da **Web.** Isso ocorre porque esses eventos não têm suporte na lógica de negócios de modelos de formulário publicados em bibliotecas de documentos no Microsoft SharePoint Server 2010 com o InfoPath Forms Services. Para criar um manipulador de eventos para o [evento ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) ou [Sign,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) você deve alterar a configuração de compatibilidade para o Formulário do Editor do **InfoPath** no InfoPath Designer. Para fazer isso, clique **na** guia Arquivo, clique em  Opções de **Formulário,** clique em Compatibilidade **e,** em seguida, de definir o tipo de formulário para o Formulário do Editor **do InfoPath.** 
  
### <a name="add-an-event-handler-for-the-submit-event-of-a-form"></a>Adicionar um manipulador de eventos para o evento Submit de um formulário

1. Abra o modelo de formulário no InfoPath Designer.
    
2. Clique na **guia** Arquivo, clique  **em Enviar para** na guia Informações e em ** Opções de Envio **.
    
3. Click **Allow users to submit this form,** click Perform custom action using **Code**, and then click **Edit Code**.
    
    O foco alterna para o manipulador de eventos esqueleto [para o evento Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) no editor de código do Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-save-event-of-a-form"></a>Adicionar um manipulador de eventos para o evento Save de um formulário

1. Abra o modelo de formulário no InfoPath Designer.
    
2. Clique na guia **Arquivo** e em **Opções de Formulário**. Depois, clique na guia **Informações**. 
    
3. Clique na **categoria** Salvar, marque **a caixa de seleção** Salvar usando código personalizado e clique em **Editar.**
    
    O foco alterna para o manipulador de eventos esqueleto do [evento Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) no editor de código do Visual Studio 2012. 
    
    > [!NOTE]
    > A **caixa de seleção** Salvar usando código personalizado não estará disponível se a configuração de compatibilidade para o modelo de formulário estiver definida como **InfoPath Forms Services**. Isso ocorre porque o evento [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) não tem suporte na lógica de negócios de modelos de formulário publicados em bibliotecas de documentos no Microsoft SharePoint Server 2010 com o InfoPath Forms Services. Para criar um manipulador de eventos para o evento [Save,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) você deve alterar a configuração de compatibilidade para o Formulário do Editor do **InfoPath** no InfoPath Designer. Para fazer isso, clique **na** guia Arquivo, clique em  Opções de **Formulário,** clique em Compatibilidade **e,** em seguida, de definir o tipo de formulário para o Formulário do Editor **do InfoPath.** 
  
### <a name="add-an-event-handler-for-the-versionupgrade-event-of-a-form"></a>Adicionar um manipulador de eventos para o evento VersionUpgrade de um formulário

1. Abra o modelo de formulário no InfoPath Designer.
    
2. Clique na guia **Arquivo** e em **Opções de Formulário**. Depois, clique na guia **Informações**. 
    
3. Clique na **categoria Versioning,** **selecione Use custom event** in the Update **existing forms** drop-down box, and then click **Edit**.
    
    O foco alterna para o manipulador de eventos esqueleto do [evento Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) no editor de código do Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-merge-event-of-a-form"></a>Adicionar um manipulador de eventos para o evento Merge de um formulário

1. Abra o modelo de formulário no InfoPath Designer.
    
2. Clique na guia **Arquivo** e em **Opções de Formulário**. Depois, clique na guia **Informações**. 
    
3. Clique na categoria **Avançado,** clique na caixa de  seleção Habilitar mesclagem de formulário, clique na caixa de seleção Mesclar usando código personalizado e clique em **Editar.** 
    
    O foco alterna para o manipulador de eventos esqueleto do [evento Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) no editor de código do Visual Studio 2012. 
    
    > [!NOTE]
    > A caixa de seleção **Habilitar** mesclação de formulários não estará disponível se a configuração de compatibilidade do modelo de formulário estiver definida como **InfoPath Forms Services**. Isso ocorre porque o evento [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) não tem suporte na lógica de negócios de modelos de formulário publicados em bibliotecas de documentos no Microsoft SharePoint Server 2010 com o InfoPath Forms Services. Para criar um manipulador de eventos para o evento [Merge,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) você deve alterar a configuração de compatibilidade para o Formulário do Editor do **InfoPath** no InfoPath Designer. Para fazer isso, clique **na** guia Arquivo, clique em  Opções de **Formulário,** clique em Compatibilidade **e,** em seguida, de definir o tipo de formulário para o Formulário do Editor **do InfoPath.** 
  
## <a name="see-also"></a>Confira também



[Passo a passo: Criando um modelo de formulário básico com código](walkthrough-creating-a-basic-form-template-with-code.md)

