---
title: Trabalhar com modos de exibição usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- modelos de formulário compatíveis com 2003 do InfoPath, exibições, exibições [InfoPath 2007], modelos de formulário compatíveis com o InfoPath 2003
localization_priority: Normal
ms.assetid: feb1bfcb-1cb1-4d5c-bc84-df86a33a5934
description: Ao trabalhar com um modelo de formulário do InfoPath, você pode escrever código para acessar os modos de exibição do formulário e, em seguida, executar uma variedade de ações nos dados que contêm os modos de exibição. O modelo de objeto compatível com o InfoPath 2003 suporta acesso aos modos de exibição de um formulário com o uso de membros da interface ViewObject.
ms.openlocfilehash: 1cbc472993ff18b26f31e3bc28b12a75e559644a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765622"
---
# <a name="work-with-views-using-the-infopath-2003-object-model"></a>Trabalhar com modos de exibição usando o modelo de objeto do InfoPath 2003

Ao trabalhar com um modelo de formulário do InfoPath, você pode escrever código para acessar os modos de exibição do formulário e, em seguida, executar uma variedade de ações nos dados que contêm os modos de exibição. O modelo de objeto compatível com o InfoPath 2003 suporta acesso aos modos de exibição de um formulário com o uso de membros da interface [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) . 
  
## <a name="overview-of-the-viewobject-interface"></a>Visão geral da Interface ViewObject

A interface de [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) oferece os seguintes métodos e propriedades, que os desenvolvedores de formulário podem usar para interagir com um modo de exibição do InfoPath. 
  
> [!NOTE]
> Os métodos e propriedades da interface [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) não estão disponíveis durante o evento [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) . 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Método [DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.DisableAutoUpdate.aspx)  <br/> |Desabilita a sincronização do modelo de objeto de documento (DOM) o XML e o modo de exibição.  <br/> |
|Método [EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.EnableAutoUpdate.aspx)  <br/> |Habilita a sincronização do DOM XML e o modo de exibição.  <br/> |
|Método [ExecuteAction](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.ExecuteAction.aspx)  <br/> |Executa uma ação de edição do InfoPath.  <br/> |
|Método [Export](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Export.aspx)  <br/> |Exporta o modo de exibição como um arquivo do formato especificado.  <br/> |
|Método [ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.ForceUpdate.aspx)  <br/> |Sincroniza o DOM XML e o modo de exibição.  <br/> |
|Método [GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.GetContextNodes.aspx)  <br/> |Retorna uma referência para a interface [XMLNodesCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XMLNodesCollection.aspx) , com base na seleção atual no modo de exibição ou o contexto de nó e o modo de exibição XML especificado.  <br/> |
|Método [GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.GetSelectedNodes.aspx)  <br/> |Retorna uma referência para a interface **XMLNodesCollection** , com base na seleção atual no modo de exibição.  <br/> |
|Método [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectNodes.aspx)  <br/> |Seleciona um intervalo de nós XML no modo de exibição.  <br/> |
|Método [SelectText](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectText.aspx)  <br/> |Seleciona o texto contido no nó XML especificado no modo de exibição.  <br/> |
|Método [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SwitchView.aspx)  <br/> |Alterna um formulário do InfoPath para o modo de exibição especificado  <br/> |
|Propriedade [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Name.aspx)  <br/> |Retorna um valor de cadeia de caracteres indicando o nome do modo de exibição atual.  <br/> |
|Propriedade [Window](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Window.aspx)  <br/> |Retorna uma referência à interface [WindowObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowObject.aspx) que acessa a **janela** associada à exibição.  <br/> |
   
> [!NOTE]
> O modelo de objeto compatível com o InfoPath 2003 também fornece a interface de [ViewInfosCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfosCollection.aspx) , que pode ser usada para obter informações sobre todas as exibições implementadas em um formulário. 
  
## <a name="using-the-viewobject-interface"></a>Usando a Interface ViewObject

A interface [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) é acessada por meio da propriedade de [modo de exibição](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.View.aspx) da interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) (que é acessado através do `thisXDocument` variável é inicializado no `_Startup` método da classe de código do formulário). Por exemplo, o exemplo de código a seguir demonstra como usar o método de [alerta](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) da interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) para exibir uma caixa de mensagem com o nome do modo de exibição atual que está associada ao documento XML subjacente de um formulário. 
  
```cs
thisXDocument.UI.Alert("Current view name: " + 
   thisXDocument.View.Name);
```

```vb
thisXDocument.UI.Alert("Current view name: " &amp; _
   thisXDocument.View.Name)
```

Todos os formulários do InfoPath contêm pelo menos um modo de exibição padrão; No entanto, o InfoPath também suporta a criação de vários modos de exibição do documento XML subjacente de um formulário. Quando você tem várias exibições em um formulário, o objeto de **modo de exibição** pode ser usado para trabalhar com o modo de exibição ativo no momento. Programaticamente, você pode alterar o modo de exibição que está ativo no momento usando o método **SwitchView** do objeto **View** , conforme o exemplo de código a seguir demonstra. 
  
```cs
thisXDocument.View.SwitchView("MySecondView");
```

```vb
thisXDocument.View.SwitchView("MySecondView")
```

O exemplo anterior para alternar entre um modo de exibição funcionará somente depois que o formulário é aberto. Para definir um modo de exibição padrão durante o evento **OnLoad** , use a propriedade [IsDefault](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.IsDefault.aspx) da interface [ViewInfoObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfoObject.aspx) , conforme mostrado no exemplo a seguir. 
  
```cs
thisXDocument.ViewInfos["MyDefaultView"].IsDefault = true;
```

```vb
thisXDocument.ViewInfos("MyDefaultView").IsDefault = True
```


