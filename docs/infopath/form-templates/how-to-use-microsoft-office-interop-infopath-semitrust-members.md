---
title: Use SemiTrust membros não é compatíveis com o InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- modelos de formulário de 2003 compatíveis do InfoPath, usando os recursos do infopath 2007
localization_priority: Normal
ms.assetid: d082f3a3-387a-4db1-bbad-495c326b8ee3
description: O modelo de objeto fornecido pelo namespace SemiTrust inclui objetos e membros que fornecem a nova funcionalidade que foi adicionada ao Office InfoPath 2007 e InfoPath.
ms.openlocfilehash: 3d0e9b450dab6a821af1f698d9859b21e85abf81
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765615"
---
# <a name="use-microsoftofficeinteropinfopathsemitrust-members-not-compatible-with-infopath"></a>Use SemiTrust membros não é compatíveis com o InfoPath

Quando você adicionar código para um modelo de formulário foi criado com o Microsoft Office InfoPath 2003 Toolkit ou cria um novo modelo de formulário que funciona com o modelo de objeto compatível com o InfoPath 2003 (conforme descrito na [criar um modelo de formulário usando o objeto do InfoPath 2003 Modelo](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)), por padrão, o Microsoft InfoPath usará um subconjunto dos objetos e membros fornecidos pelo namespace [SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) que são idênticas às usadas pelo InfoPath 2003. Isso é feito para fornecer compatibilidade com o InfoPath 2003. No entanto, o modelo de objeto fornecido pelo namespace [SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) inclui objetos adicionais e os membros que fornecem a nova funcionalidade que foi adicionada ao Office InfoPath 2007 e InfoPath. 
  
Por exemplo, as interfaces de [permissão](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) e [PermissionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) fornecem a nova funcionalidade de gerenciamento de direitos de informação que não está disponível no InfoPath 2003. Este e outros novos objetos adicionados ao namespace SemiTrust não estão disponíveis por padrão quando você abre ou cria um modelo de formulário de código gerenciado com o modelo de objeto compatível com o InfoPath 2003. 
  
Da mesma forma, enquanto o [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) interface oferece a mesma funcionalidade que o InfoPath 2003; a interface de [_XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) foi versionada para incluir propriedades e métodos que foram adicionados no Office InfoPath 2007 adicionais e o [_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) ficou versionado para incluir propriedades e métodos que foram adicionados no InfoPath adicionais . 
  
Se você deseja usar objetos e membros que foram adicionados no Office InfoPath 2007 ou InfoPath em um projeto de modelo de formulário criado usando o modelo de objeto fornecido pelo namespace **SemiTrust** , você poderá fazer isso, mas o código que usa Esses membros não será compatíveis com o InfoPath 2003. 
  
> [!NOTE]
> Todos os modelos de formulário com lógica de negócios criados usando o modelo de objeto fornecido pelo namespace **SemiTrust** , se eles usam objetos e membros compatíveis com o InfoPath ou não, não há suporte para modelos de formulário habilitados para navegador implantados para Microsoft SharePoint Server 2010 com o InfoPath Forms Services. A lógica de negócios para modelos de formulário habilitados para navegador deve usar o novo modelo de objeto de código gerenciado do InfoPath fornecido pelo namespace [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) . 
  
## <a name="example"></a>Example

### <a name="creating-an-xdocument-or-application-object-variable-to-access-new-object-model-members"></a>Criando um XDocument ou a variável de objeto de aplicativo para o Access novos membros do modelo de objeto

Para acessar os novos objetos e membros que estão disponíveis no namespace **SemiTrust** , você deve declarar e convertida de variáveis de objeto para a versão correta da interface que implementa esses membros. Por padrão, o `thisXDocument` e `thisApplication` variáveis acessar as versões compatíveis com o InfoPath 2003 do correspondente **_XDocument2** e interfaces [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) . Para acessar as interfaces **_XDocument3** e [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) que fornecem acesso a nova funcionalidade, você deve declarar uma variável de objeto do tipo **_XDocument3** ou **_Application3** e difundir o objeto retornado pelo `thisXDocument`ou `thisApplication` variável para o mesmo tipo, conforme mostrado nos exemplos a seguir. 
  
```cs
// Declare an object variable of type _XDocument3 and
// cast the object returned by the thisXDocument variable to
// the same type.
_XDocument3 thisXDocument3 = (_XDocument3)thisXDocument;
```

```vb
' Declare an object variable of type _XDocument3 and
' cast the object returned by the thisXDocument variable to
' the same type.
Dim thisXDocument3 As _XDocument3 = _
   DirectCast(thisXDocument, _XDocument3)
```

```cs
// Declare an object variable of type _Application3 and
// cast the object returned by the thisApplication variable to
// the same type.
_Application3 thisApplication3 = (_Application3)thisXDocument;
```

```vb
' Declare an object variable of type _Application3 and
' cast the object returned by the thisXApplication variable to
' the same type.
Dim thisDocument As _XDocument3 = _
   DirectCast(thisXDocument, _XDocument3)
```

### <a name="accessing-a-new-object-from-the-xdocument-or-application-object-variable-using-an-accessor-property"></a>Acessando um novo objeto na variável de objeto de aplicativo, usando uma propriedade de acessador ou XDocument

Depois de criar uma variável do _ versão posterior **XDocument3** ou tipo de **_Application3** , você pode usá-lo para acessar um objeto ou membro que fornece a nova funcionalidade do InfoPath. 
  
O exemplo a seguir mostra como usar uma variável de objeto do tipo _ **XDocument3** com a propriedade de acessador de [permissão](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) para acessar a nova interface de **permissão** e sua propriedade [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) para determinar se as configurações de permissão são habilitado para o formulário. 
  
```cs
// Declare an object variable of type _XDocument3 and
// cast the object returned by the thisXDocument variable to
// the same type.
_XDocument3 thisXDocument3 = (_XDocument3)thisXDocument;
// Use the object variable to access the later version object and
// property.
thisXDocument.UI.Alert(thisDocument3.Permission.Enabled.ToString());
```

```vb
' Declare an object variable of type _XDocument3 and
' cast the object returned by the thisXDocument variable to
' the same type.
Dim thisXDocument3 As _XDocument3 = _
   DirectCast(thisXDocument, _XDocument3)
' Use the object variable to access the later version object and
' property.
thisXDocument.UI.Alert(thisDocument3.Permission.Enabled.ToString())
```

### <a name="accessing-a-versioned-object-and-casting-to-the-versioned-type"></a>Acessando um objeto versionado e projeção para o tipo de versionado

Se um objeto que existia no modelo de objeto do InfoPath 2003 tiver novas propriedades ou métodos adicionados a ela, o objeto que implementa esses novos membros terá um nome que for atualizado.
  
Por exemplo, o objeto [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) não fornece acesso a duas novas propriedades que só estão disponíveis ao usar o objeto de [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) versionado: as propriedades [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) e [HideName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) . 
  
Para acessar essas propriedades, você deve declarar uma variável de objeto do tipo **ViewInfo2** e converter o objeto retornado pela propriedade [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) da variável de objeto _ **XDocument3** para o tipo de **ViewInfo2** , conforme mostrado no seguinte exemplo. 
  
```cs
// Declare an object variable of type _XDocument3 and
// cast the object returned by the thisXDocument variable to
// the same type.
_XDocument3 thisXDocument3 = (_XDocument3)thisXDocument;
// Declare an object variable of type ViewInfo2 and cast the object 
// returned by the ViewInfos property to that type.
ViewInfo2 thisView = (ViewInfo2)thisXDocument3.ViewInfos["View2"];
// Display the value of the new HideName property.
thisXDocument3.UI.Alert(thisView.HideName.ToString());
```

```vb
' Declare an object variable of type _XDocument3 and
' cast the object returned by the thisXDocument variable to
' the same type.
Dim thisXDocument3 As _XDocument3 = _
   DirectCast(thisXDocument, _XDocument3)
' Declare an object variable of type ViewInfo2 and cast the object 
' returned by the ViewInfos property to that type.
Dim thisView As ViewInfo2 = _
   DirectCast(thisXDocument3.ViewInfos("View2"), ViewInfo2)
' Display the value of the new HideName property.
thisXDocument3.UI.Alert(thisView.HideName.ToString())
```


