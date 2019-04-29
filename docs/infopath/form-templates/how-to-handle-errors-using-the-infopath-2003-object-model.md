---
title: Manipular erros usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- modelos de formulário compatíveis com o InfoPath 2003, tratamento de erros, modelos de formulário compatíveis com o InfoPath 2003, tratamento de erros, modelos de formulário [InfoPath 2007], tratamento de erros, tratamento de erros [InfoPath 2007], modelos de formulário compatíveis com o InfoPath 2003
localization_priority: Normal
ms.assetid: eeb05205-d6f4-4931-b9a9-55a663bb1a25
description: Ao criar aplicativos personalizados, os desenvolvedores geralmente devem realizar o tratamento de erros que envolve a gravação do código de programação para verificar se há erros gerados pelo aplicativo ou para criar e gerar erros personalizados. O modelo de objeto compatível com o InfoPath 2003 oferece suporte ao tratamento de erros através do uso do objeto ErrorObject em associação com a coleção Errors.
ms.openlocfilehash: 93991e33d8867f89454bec08b41ba83e98ab0a17
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439475"
---
# <a name="handle-errors-using-the-infopath-2003-object-model"></a>Manipular erros usando o modelo de objeto do InfoPath 2003

Ao criar aplicativos personalizados, os desenvolvedores geralmente devem realizar o tratamento de erros que envolve a gravação do código de programação para verificar se há erros gerados pelo aplicativo ou para criar e gerar erros personalizados. O modelo de objeto compatível com o InfoPath 2003 oferece suporte ao tratamento de erros [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorObject.aspx) através do uso do objeto ErrorObject em associação com a coleção [Errors](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorsCollection.aspx) . 
  
No InfoPath, os erros podem ocorrer quando os dados inseridos em um formulário falham na validação de esquema XML, quando uma restrição de validação personalizada falha, quando um erro é gerado pelo método [ReportError](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReportError.aspx) do objeto datadomeventobject ou quando um erro é criado [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEventObject.aspx) usando o método [Add](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Add.aspx) da coleção [Errors](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorsCollection.aspx) . 
  
## <a name="overview-of-the-errorscollection-collection"></a>Visão geral da coleção Errors

A **** coleção Errors fornece os seguintes métodos e propriedades, que os desenvolvedores de formulários podem usar para gerenciar os objetos **ErrorObject** contidos na coleção. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Método[Adicionar](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Add.aspx)  <br/> |Cria um **** objeto ErrorObject e o adiciona à coleção.  <br/> |
|Método[Excluir](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Delete.aspx)  <br/> |Exclui todos **** os objetos ErrorObject associados ao nó XML especificado e ao nome da condição, exceto erros personalizados adicionados usando o método **ReportError** .  <br/> |
|Método [DeleteAll](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.DeleteAll.aspx)  <br/> |Exclui todos **** os objetos ErrorObject contidos na coleção.  <br/> |
|Propriedade [Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Count.aspx)  <br/> |Obtém uma contagem do número de objetos **ErrorObject** contidos na coleção.  <br/> |
|Propriedade [Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Item.aspx)  <br/> |Obtém uma referência a um **** objeto ErrorObject com base no número de índice especificado.  <br/> |
   
## <a name="overview-of-the-errorobject-object"></a>Visão geral do objeto ErrorObject

O **** objeto ErrorObject fornece as seguintes propriedades, que os desenvolvedores de formulários podem usar para acessar informações sobre o erro que foi gerado. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|[](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ConditionName.aspx) Propriedade ConditionName  <br/> |Obtém o nome da condição de erro ou retorna **NULL**, dependendo do tipo de objeto ErrorObject **** .  <br/> |
|Propriedade [DetailedErrorMessage](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.DetailedErrorMessage.aspx)  <br/> |Obtém ou define a mensagem de erro detalhada do **** objeto ErrorObject.  <br/> |
|Propriedade [ErrorCode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ErrorCode.aspx)  <br/> |Obtém ou define o código de erro do **** objeto ErrorObject.  <br/> |
|Propriedade [node](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.Node.aspx)  <br/> |Obtém uma referência ao nó XML associado ao objeto **ErrorObject** .  <br/> |
|Propriedade [ShortErrorMessage](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ShortErrorMessage.aspx)  <br/> |Obtém ou define a mensagem de erro curta do **** objeto ErrorObject.  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ErrorType.aspx) Propriedade ErrorType  <br/> |Obtém o tipo do objeto **ErrorObject** .  <br/> |
   
## <a name="using-the-errorscollection-and-errorobject"></a>Usando os Erroscollection e ErrorObject

A **** coleção Errors é acessada por meio da propriedade [Errors](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument.Errors.aspx) do objeto [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) . A **** coleção Errors é associada ao documento XML subjacente de um formulário para que, quando ocorrer um erro, ele ocorra no documento XML. O exemplo a seguir demonstra como um loop **foreach** do Visual C# pode ser usado para verificar os erros que podem existir no documento XML subjacente de um formulário. Se houver erros, a função entrará em loop por cada um deles e, usando a propriedade **ShortErrorMessage** do objeto **ErrorObject** , exibirá uma caixa de mensagem para o usuário. 
  
```cs
public void CheckErrors(IXMLDOMNode xmlNode)
{
   foreach(ErrorObject err in thisXDocument.Errors)
   {
      if(xmlNode==err.Node)
         thisXDocument.UI.Alert("The following error has occured: "
             + err.ShortErrorMessage + ".");
   }
}
```

A função precedente pode ser chamada de um dos manipuladores de eventos de validação de dados do formulário. Por exemplo, quando usado no manipulador de eventos [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) para um campo no formulário, a chamada para a função passa o argumento de nó XML usando a propriedade [site](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.Site.aspx) do objeto datadomeventobject da seguinte maneira. [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEventObject.aspx) 
  
```cs
CheckErrors(e.Site);
```

Além de lidar com erros gerados pelo InfoPath, os desenvolvedores de formulários também podem gerar erros personalizados usando o método **ReportError** do **** objeto datadomeventobject ou usando o método **Add** do **errocollection** coletânea. Para obter informações sobre como usar os métodos **ReportError** ou **Add** , clique nos métodos no início deste tópico. 
  
## <a name="handling-managed-code-exceptions"></a>Tratamento de exceções de código gerenciado

Você pode usar a manipulação de exceção de try-catch para lidar com exceções geradas no modelo de formulário de código gerenciado, conforme mostrado no exemplo de código a seguir.
  
```cs
DataAdapters dataAdapters;
dataAdapters = thisXDocument.DataAdapters; 
XMLFileAdapterObject queryXMLFile = 
   (XMLFileAdapterObject)dataAdapters["form1"];
// Perform the query.
try
{
   queryXMLFile.Query();
}
catch (Exception ex)
{
   thisXDocument.UI.Alert("Failed to query.\n\n" + ex.Message);
}
// Perform the submit.
try
{
   queryXMLFile.Submit();
}
catch (Exception ex)
{
   thisXDocument.UI.Alert("Failed to submit.\n\n" + ex.Message);
}
```

Se você não usar a manipulação de exceção de tentativa-catch no seu código de formulário, o InfoPath exibirá informações sobre exceções não tratadas na caixa de diálogo de erro do InfoPath durante a depuração e a visualização. 
  

