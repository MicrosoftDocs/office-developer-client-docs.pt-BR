---
title: Lidar com erros usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- modelos de formulário compatíveis com 2003 do InfoPath, tratamento de erros, modelos de formulário compatíveis com o InfoPath 2003, tratamento de erros, modelos de formulário [InfoPath 2007], tratamento de erros, [InfoPath 2007] de tratamento de erros, modelos de formulário compatíveis com o InfoPath 2003
localization_priority: Normal
ms.assetid: eeb05205-d6f4-4931-b9a9-55a663bb1a25
description: Ao criar aplicativos personalizados, os desenvolvedores devem frequentemente executar tratamento de erros que envolve escrever códigos de programação para verificar erros gerados pelo aplicativo ou para criar e gerar erros personalizados. O modelo de objeto compatível com o InfoPath 2003 oferece suporte com o uso do objeto ErrorObject em associação com a coleção ErrorsCollection de tratamento de erros.
ms.openlocfilehash: 577e531d8943dc8fc3884cd81f68b11ca285c5d3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765628"
---
# <a name="handle-errors-using-the-infopath-2003-object-model"></a>Lidar com erros usando o modelo de objeto do InfoPath 2003

Ao criar aplicativos personalizados, os desenvolvedores devem frequentemente executar tratamento de erros que envolve escrever códigos de programação para verificar erros gerados pelo aplicativo ou para criar e gerar erros personalizados. O modelo de objeto compatível com o InfoPath 2003 oferece suporte com o uso do objeto [ErrorObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorObject.aspx) em associação com a coleção [ErrorsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorsCollection.aspx) de tratamento de erros. 
  
No InfoPath, os erros podem ocorrer quando os dados inseridos em um formulário falhar validação de esquema XML, quando uma restrição de validação personalizada falha, quando um erro é gerado pelo método do objeto [DataDOMEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEventObject.aspx) [ReportError](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReportError.aspx) ou quando um erro é criado usando o método [Add](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Add.aspx) da coleção [ErrorsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorsCollection.aspx) . 
  
## <a name="overview-of-the-errorscollection-collection"></a>Visão geral da coleção ErrorsCollection

A coleção de **ErrorsCollection** fornece os seguintes métodos e propriedades, que os desenvolvedores de formulário podem usar para gerenciar os objetos **ErrorObject** contido na coleção. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Método [Add](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Add.aspx)  <br/> |Cria um objeto **ErrorObject** e o adiciona à coleção.  <br/> |
|Método [Delete](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Delete.aspx)  <br/> |Exclui todos os objetos de **ErrorObject** associados com o XML nó e a condição nome especificado, exceto para erros personalizados adicionados usando o método **ReportError** .  <br/> |
|Método [DeleteAll](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.DeleteAll.aspx)  <br/> |Exclui todos os objetos **ErrorObject** contidos na coleção.  <br/> |
|Propriedade [Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Count.aspx)  <br/> |Obtém uma contagem do número de objetos **ErrorObject** contido na coleção.  <br/> |
|Propriedade [item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Item.aspx)  <br/> |Obtém uma referência a um objeto **ErrorObject** com base no número de índice especificado.  <br/> |
   
## <a name="overview-of-the-errorobject-object"></a>Visão geral do objeto ErrorObject

O objeto de **ErrorObject** fornece as seguintes propriedades, os desenvolvedores de formulário podem usar para acessar informações sobre o erro que foi gerado. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Propriedade [ConditionName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ConditionName.aspx)  <br/> |Obtém o nome da condição de erro ou retorna **null**, dependendo do tipo de objeto **ErrorObject** .  <br/> |
|Propriedade [DetailedErrorMessage](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.DetailedErrorMessage.aspx)  <br/> |Obtém ou define a mensagem de erro detalhadas do objeto **ErrorObject** .  <br/> |
|Propriedade [ErrorCode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ErrorCode.aspx)  <br/> |Obtém ou define o código de erro do objeto **ErrorObject** .  <br/> |
|Propriedade [Node](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.Node.aspx)  <br/> |Obtém uma referência ao nó XML associado ao objeto **ErrorObject** .  <br/> |
|Propriedade [ShortErrorMessage](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ShortErrorMessage.aspx)  <br/> |Obtém ou define a mensagem de erro curta do objeto **ErrorObject** .  <br/> |
|Propriedade [ErrorType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ErrorType.aspx)  <br/> |Obtém o tipo do objeto **ErrorObject** .  <br/> |
   
## <a name="using-the-errorscollection-and-errorobject"></a>Usando o ErrorsCollection e ErrorObject

A coleção de **ErrorsCollection** é acessada por meio da propriedade [erros](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument.Errors.aspx) do objeto [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) . A coleção **ErrorsCollection** é associada ao documento XML subjacente de um formulário, para que quando ocorre um erro, ele ocorra dentro do documento XML. O exemplo a seguir demonstra como um loop **foreach** Visual c# pode ser usado para verificar os erros que podem existir no documento XML subjacente de um formulário. Se houver erros, a função faz um loop por cada um deles e, usando a propriedade **ShortErrorMessage** do objeto **ErrorObject** , exibe uma caixa de mensagem para o usuário. 
  
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

A função anterior poderia ser chamada de um dos manipuladores de eventos de validação de dados do formulário. Por exemplo, quando usado no manipulador de eventos [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) para um campo no formulário, a chamada para a função seria passar o argumento do nó XML usando a propriedade do [Site](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.Site.aspx) do objeto [DataDOMEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEventObject.aspx) como se segue. 
  
```cs
CheckErrors(e.Site);
```

Além de tratamento de erros gerados pelo InfoPath, os desenvolvedores de formulário também podem o gerar erros personalizados usando o método **ReportError** do objeto **DataDOMEventObject** ou usando o método **Add** do **ErrorsCollection** coleção. Para obter informações sobre como usar os métodos **ReportError** ou **Adicionar** , clique nos métodos no início deste tópico. 
  
## <a name="handling-managed-code-exceptions"></a>Tratamento de exceções de código gerenciado

Você pode usar o tratamento de exceção de try-catch para manipular exceções geradas no modelo de formulário de código gerenciado, conforme mostrado no exemplo de código a seguir.
  
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

Se você não usar try-catch de tratamento de exceção no seu código de formulário, o InfoPath exibirá informações sobre exceções não tratadas na caixa de diálogo de erro do InfoPath durante a depuração e visualização. 
  

