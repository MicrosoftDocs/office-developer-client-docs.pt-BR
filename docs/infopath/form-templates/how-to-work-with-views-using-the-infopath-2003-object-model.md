---
title: Trabalhar com modos de exibição usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- modelos de formulário compatíveis com o InfoPath 2003, modos de exibição, modos de exibição [InfoPath 2007], modelos de formulário compatíveis com o InfoPath 2003
localization_priority: Normal
ms.assetid: feb1bfcb-1cb1-4d5c-bc84-df86a33a5934
description: Ao trabalhar com um modelo de formulário do InfoPath, você pode escrever código para acessar os modos de exibição do formulário e, em seguida, executar uma variedade de ações nos dados que os modos de exibição contêm. O modelo de objeto compatível com o InfoPath 2003 oferece suporte ao acesso a modos de exibição de um formulário por meio do uso dos membros da interface Viewobject.
ms.openlocfilehash: 6a2dd408ba51e5c8394120944e0c28897e768738
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299873"
---
# <a name="work-with-views-using-the-infopath-2003-object-model"></a>Trabalhar com modos de exibição usando o modelo de objeto do InfoPath 2003

Ao trabalhar com um modelo de formulário do InfoPath, você pode escrever código para acessar os modos de exibição do formulário e, em seguida, executar uma variedade de ações nos dados que os modos de exibição contêm. O modelo de objeto compatível com o InfoPath 2003 oferece suporte ao acesso a modos de exibição de um formulário por meio [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) do uso dos membros da interface viewobject. 
  
## <a name="overview-of-the-viewobject-interface"></a>Visão geral da interface Viewobject

A [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) interface viewobject fornece os seguintes métodos e propriedades, que os desenvolvedores de formulários podem usar para interagir com um modo de exibição do InfoPath. 
  
> [!NOTE]
> Os métodos e as propriedades da [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) interface viewobject não estão disponíveis durante o evento [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) . 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Método [DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.DisableAutoUpdate.aspx)  <br/> |Desabilita a sincronização do DOM (modelo de objeto do documento) XML e o modo de exibição.  <br/> |
|Método [EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.EnableAutoUpdate.aspx)  <br/> |Permite a sincronização do DOM XML e do modo de exibição.  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.ExecuteAction.aspx) Método ExecuteAction  <br/> |Executa uma ação de edição do InfoPath.  <br/> |
|Método [Export](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Export.aspx)  <br/> |Exporta o modo de exibição como um arquivo do formato especificado.  <br/> |
|Método [ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.ForceUpdate.aspx)  <br/> |Sincroniza o XML DOM e o modo de exibição.  <br/> |
|Método [GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.GetContextNodes.aspx)  <br/> |Retorna uma referência à interface [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XMLNodesCollection.aspx) xmlnodecollection, com base no nó XML especificado e no contexto de exibição ou na seleção atual no modo de exibição.  <br/> |
|Método [GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.GetSelectedNodes.aspx)  <br/> |Retorna uma referência à interface **** xmlnodecollection, com base na seleção atual no modo de exibição.  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectNodes.aspx) Método SelectNodes  <br/> |Seleciona um intervalo de nós XML no modo de exibição.  <br/> |
|Método [SelectText](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectText.aspx)  <br/> |Seleciona o texto contido no nó XML especificado no modo de exibição.  <br/> |
|Método [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SwitchView.aspx)  <br/> |Alterna um formulário do InfoPath para o modo de exibição especificado  <br/> |
|Propriedade [Nome](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Name.aspx)  <br/> |Retorna um valor String que indica o nome do modo de exibição atual.  <br/> |
|Propriedade [Window](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Window.aspx)  <br/> |Retorna uma referência à interface [WindowObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowObject.aspx) que acessa a **janela** associada ao modo de exibição.  <br/> |
   
> [!NOTE]
> O modelo de objeto compatível com o InfoPath 2003 também fornece a interface [ViewInfosCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfosCollection.aspx) , que pode ser usada para obter informações sobre todos os modos de exibição implementados em um formulário. 
  
## <a name="using-the-viewobject-interface"></a>Usando a interface Viewobject

A [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) interface viewobject é acessada por meio da propriedade [View](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.View.aspx) da interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) (que é acessada por meio da `thisXDocument` variável `_Startup` que é inicializada no método da classe de código de formulário). Por exemplo, o exemplo de código a seguir demonstra como usar o método de [alerta](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) da interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) para exibir uma caixa de mensagem com o nome do modo de exibição atual que está associado ao documento XML subjacente de um formulário. 
  
```cs
thisXDocument.UI.Alert("Current view name: " + 
   thisXDocument.View.Name);
```

```vb
thisXDocument.UI.Alert("Current view name: " &amp; _
   thisXDocument.View.Name)
```

Todos os formulários do InfoPath contêm pelo menos um modo de exibição padrão; no entanto, o InfoPath também dá suporte à criação de vários modos de exibição do documento XML subjacente de um formulário. Quando você tem vários modos de exibição em um formulário, o objeto **View** pode ser usado para trabalhar com o modo de exibição ativo no momento. Você pode alterar programaticamente o modo de exibição que está ativo no momento usando o método **SwitchView** do objeto **View** , como mostra o exemplo de código a seguir. 
  
```cs
thisXDocument.View.SwitchView("MySecondView");
```

```vb
thisXDocument.View.SwitchView("MySecondView")
```

O exemplo anterior para mudar de um modo de exibição funcionará somente depois que o formulário for aberto. Para definir um modo de exibição padrão durante o evento **OnLoad** , use a Propriedade IsDefault da interface [ViewInfoObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfoObject.aspx) , conforme mostrado no exemplo a seguir. [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.IsDefault.aspx) 
  
```cs
thisXDocument.ViewInfos["MyDefaultView"].IsDefault = true;
```

```vb
thisXDocument.ViewInfos("MyDefaultView").IsDefault = True
```


