---
title: Trabalhar com exibições usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- modelos de formulário compatíveis com InfoPath 2003, exibições, exibições [InfoPath 2007], modelos de formulário compatíveis com InfoPath 2003
localization_priority: Normal
ms.assetid: feb1bfcb-1cb1-4d5c-bc84-df86a33a5934
description: Ao trabalhar com um modelo de formulário do InfoPath, você pode escrever código para acessar as exibições do formulário e, em seguida, executar uma variedade de ações nos dados que os exibições contêm. O modelo de objeto compatível com o InfoPath 2003 dá suporte ao acesso a exibições de um formulário por meio do uso dos membros da interface ViewObject.
ms.openlocfilehash: 6a2dd408ba51e5c8394120944e0c28897e768738
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411880"
---
# <a name="work-with-views-using-the-infopath-2003-object-model"></a>Trabalhar com exibições usando o modelo de objeto do InfoPath 2003

When working with an InfoPath form template, you can write code to access the form's views, and then perform a variety of actions on the data that the views contain. O modelo de objeto compatível com o InfoPath 2003 dá suporte ao acesso a exibições de um formulário por meio do uso dos membros da interface [ViewObject.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) 
  
## <a name="overview-of-the-viewobject-interface"></a>Visão geral da interface ViewObject

A interface [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) fornece os seguintes métodos e propriedades, que os desenvolvedores de formulário podem usar para interagir com um modo de exibição do InfoPath. 
  
> [!NOTE]
> Os métodos e as propriedades da interface [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) não estão disponíveis durante o [evento OnLoad.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|[Método DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.DisableAutoUpdate.aspx)  <br/> |Desabilita a sincronização do MODELO de Objeto de Documento XML (DOM) e do modo de exibição.  <br/> |
|[Método EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.EnableAutoUpdate.aspx)  <br/> |Habilita a sincronização do DOM XML e do modo de exibição.  <br/> |
|[Método ExecuteAction](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.ExecuteAction.aspx)  <br/> |Executa uma ação de edição do InfoPath.  <br/> |
|[Método Export](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Export.aspx)  <br/> |Exporta o exibição como um arquivo do formato especificado.  <br/> |
|[Método ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.ForceUpdate.aspx)  <br/> |Sincroniza o DOM XML e o visualização.  <br/> |
|[Método GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.GetContextNodes.aspx)  <br/> |Retorna uma referência à interface [XMLNodesCollection,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XMLNodesCollection.aspx) com base no nó XML especificado e no contexto de exibição ou na seleção atual na exibição.  <br/> |
|Método [GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.GetSelectedNodes.aspx)  <br/> |Retorna uma referência à interface **XMLNodesCollection,** com base na seleção atual no ponto de vista.  <br/> |
|[Método SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectNodes.aspx)  <br/> |Seleciona um intervalo de nós XML no visualização.  <br/> |
|[Método SelectText](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectText.aspx)  <br/> |Seleciona o texto contido no nó XML especificado no visualização.  <br/> |
|[Método SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SwitchView.aspx)  <br/> |Alterna um formulário do InfoPath para o modo de exibição especificado  <br/> |
|Propriedade [Nome](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Name.aspx)  <br/> |Retorna um valor de cadeia de caracteres indicando o nome do exibição atual.  <br/> |
|[Propriedade Window](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Window.aspx)  <br/> |Retorna uma referência à interface [WindowObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowObject.aspx) que acessa a **janela** associada ao ponto de exibição.  <br/> |
   
> [!NOTE]
> O modelo de objeto compatível com InfoPath 2003 também fornece a interface [ViewInfosCollection,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfosCollection.aspx) que pode ser usada para obter informações sobre todos os exibições implementados em um formulário. 
  
## <a name="using-the-viewobject-interface"></a>Usando a interface ViewObject

A interface [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) é acessada por meio da propriedade [View](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.View.aspx) da interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) (que é acessada por meio da variável inicializada no método da classe de código  `thisXDocument` do  `_Startup` formulário). Por exemplo, o exemplo de código a seguir demonstra como usar o método [Alerta](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) da interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) para exibir uma caixa de mensagem com o nome do modo de exibição atual associado ao documento XML subjacente de um formulário. 
  
```cs
thisXDocument.UI.Alert("Current view name: " + 
   thisXDocument.View.Name);
```

```vb
thisXDocument.UI.Alert("Current view name: " &amp; _
   thisXDocument.View.Name)
```

Todos os formulários do InfoPath contêm pelo menos um modo de exibição padrão; No entanto, o InfoPath também oferece suporte à criação de várias exibições do documento XML subjacente de um formulário. Quando você tem vários exibições em um formulário, o objeto **View** pode ser usado para trabalhar com o ponto de vista que está ativo no momento. Você pode alterar programaticamente o modo de exibição atualmente ativo usando o método **SwitchView** do objeto **View,** como demonstra o exemplo de código a seguir. 
  
```cs
thisXDocument.View.SwitchView("MySecondView");
```

```vb
thisXDocument.View.SwitchView("MySecondView")
```

O exemplo anterior para alternar um ponto de vista funcionará somente depois que o formulário for aberto. Para definir um modo de exibição padrão durante o evento **OnLoad,** use a propriedade [IsDefault](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.IsDefault.aspx) da interface [ViewInfoObject,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfoObject.aspx) conforme mostrado no exemplo a seguir. 
  
```cs
thisXDocument.ViewInfos["MyDefaultView"].IsDefault = true;
```

```vb
thisXDocument.ViewInfos("MyDefaultView").IsDefault = True
```


