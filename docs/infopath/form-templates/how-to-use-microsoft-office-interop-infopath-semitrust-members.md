---
title: Usar membros Microsoft.Office.Interop.InfoPath.SemiTrust incompatíveis com o InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- modelos de formulário compatíveis com infopath 2003, usando recursos do infopath 2007
localization_priority: Normal
ms.assetid: d082f3a3-387a-4db1-bbad-495c326b8ee3
description: O modelo de objeto fornecido pelo namespace Microsoft.Office.Interop.InfoPath.SemiTrust inclui objetos e membros que fornecem novas funcionalidades adicionadas ao Office InfoPath 2007 e ao InfoPath.
ms.openlocfilehash: 45f7607aec8ccfd653780a550df0823730835a86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415338"
---
# <a name="use-microsoftofficeinteropinfopathsemitrust-members-not-compatible-with-infopath"></a>Usar membros Microsoft.Office.Interop.InfoPath.SemiTrust incompatíveis com o InfoPath

Quando você adiciona código a um modelo de formulário criado com o Kit de Ferramentas do Microsoft Office InfoPath 2003 ou cria um novo modelo de formulário que funciona com o modelo de objeto compatível com o InfoPath 2003 (conforme descrito em [Create a Form Template Using the InfoPath 2003 Object Model](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)), por padrão, O Microsoft InfoPath usará um subconjunto dos objetos e membros fornecidos pelo namespace [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) que são idênticos aos usados pelo InfoPath 2003. Isso é feito para fornecer compatibilidade com o InfoPath 2003. No entanto, o modelo de objeto fornecido pelo namespace [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) inclui objetos e membros adicionais que fornecem novas funcionalidades adicionadas ao Office InfoPath 2007 e ao InfoPath. 
  
Por exemplo, as interfaces [PermissionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) e [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) fornecem uma nova funcionalidade de gerenciamento de direitos de informação que não está disponível no InfoPath 2003. This, and other new objects added to the Microsoft.Office.Interop.InfoPath.SemiTrust namespace are not available by default when you open or create managed code form template with InfoPath 2003-compatible object model. 
  
Da mesma forma, enquanto [a interface _XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) interface fornece a mesma funcionalidade que o InfoPath 2003; a [interface _XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) foi versionada para incluir propriedades e métodos adicionais que foram adicionados no Office InfoPath 2007, e o [_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) foi versionado para incluir propriedades e métodos adicionais que foram adicionados no InfoPath. 
  
Se você quiser usar objetos e membros que foram adicionados no Office InfoPath 2007 ou no InfoPath em um projeto de modelo de formulário criado usando o modelo de objeto fornecido pelo namespace **Microsoft.Office.Interop.InfoPath.SemiTrust,** você pode fazer isso, mas o código que usa esses membros não será compatível com o InfoPath 2003. 
  
> [!NOTE]
> Todos os modelos de formulário com lógica comercial criada usando o modelo de objeto fornecido pelo namespace **Microsoft.Office.Interop.InfoPath.SemiTrust,** independentemente de usarem objetos e membros compatíveis com o InfoPath ou não, não têm suporte para modelos de formulário habilitados para navegador implantados no Microsoft SharePoint Server 2010 com o InfoPath Forms Services. A lógica de negócios para modelos de formulário habilitados para navegador deve usar o novo modelo de objeto de código gerenciado do InfoPath fornecido pelo namespace [Microsoft.Office.InfoPath.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 
  
## <a name="example"></a>Exemplo

### <a name="creating-an-xdocument-or-application-object-variable-to-access-new-object-model-members"></a>Criando uma variável de objeto XDocument ou Application para acessar novos membros do modelo de objeto

Para acessar os novos objetos e membros disponíveis no namespace **Microsoft.Office.Interop.InfoPath.SemiTrust,** você deve declarar e lançar variáveis de objeto para a versão correta da interface que implementa esses membros. Por padrão, as variáveis e as variáveis acessam as versões compatíveis com  `thisXDocument`  `thisApplication` o InfoPath 2003 das interfaces **_XDocument2** e [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) correspondentes. Para acessar as interfaces **_XDocument3** e _Application3 que fornecem acesso à nova funcionalidade, você deve declarar uma variável de objeto do tipo **_XDocument3** ou _Application3 e, em seguida, lançar o objeto retornado pela ou [variável](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) para o mesmo tipo, conforme mostrado nos exemplos **a** `thisXDocument` `thisApplication` seguir. 
  
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

### <a name="accessing-a-new-object-from-the-xdocument-or-application-object-variable-using-an-accessor-property"></a>Acessando um novo objeto da variável XDocument ou do objeto Application usando uma propriedade Accessor

Depois de criar uma variável do tipo versão posterior _ **XDocument3** ou **_Application3,** você poderá usá-la para acessar um objeto ou membro que fornece a nova funcionalidade do InfoPath. 
  
O exemplo a seguir mostra como usar uma variável de [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) objeto do tipo _ **XDocument3** com a propriedade de acessador De permissão para acessar a nova **interface** de permissão e sua propriedade [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) para determinar se as configurações de permissão estão habilitadas para o formulário. 
  
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

### <a name="accessing-a-versioned-object-and-casting-to-the-versioned-type"></a>Acessando um objeto versionado e transmissão para o tipo versionado

Se um objeto que existia no modelo de objeto do InfoPath 2003 tiver novas propriedades ou métodos adicionados a ele, o objeto que implementa esses novos membros terá um nome com versão.
  
Por exemplo, o objeto [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) não fornece acesso a duas novas propriedades que só estão disponíveis ao usar o objeto [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) com versão: as propriedades [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) e [HideName.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) 
  
Para acessar essas propriedades, você deve declarar uma variável de objeto do tipo **ViewInfo2** e lançar o objeto retornado pela propriedade [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) da variável de objeto _ **XDocument3** para o tipo **ViewInfo2** conforme mostrado no exemplo a seguir. 
  
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


