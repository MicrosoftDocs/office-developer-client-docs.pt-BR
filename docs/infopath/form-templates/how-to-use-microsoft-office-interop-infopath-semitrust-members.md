---
title: Usar os membros Microsoft. Office. Interop. InfoPath. SemiTrust não compatíveis com o InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- modelos de formulário compatíveis com o InfoPath 2003, usando recursos do InfoPath 2007
localization_priority: Normal
ms.assetid: d082f3a3-387a-4db1-bbad-495c326b8ee3
description: O modelo de objeto fornecido pelo namespace Microsoft. Office. Interop. InfoPath. SemiTrust inclui objetos e membros que oferecem novas funcionalidades que foram adicionadas ao Office InfoPath 2007 e ao InfoPath.
ms.openlocfilehash: 45f7607aec8ccfd653780a550df0823730835a86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415338"
---
# <a name="use-microsoftofficeinteropinfopathsemitrust-members-not-compatible-with-infopath"></a><span data-ttu-id="035be-104">Usar os membros Microsoft. Office. Interop. InfoPath. SemiTrust não compatíveis com o InfoPath</span><span class="sxs-lookup"><span data-stu-id="035be-104">Use Microsoft.Office.Interop.InfoPath.SemiTrust members not compatible with InfoPath</span></span>

<span data-ttu-id="035be-105">Quando você adiciona código a um modelo de formulário criado com o kit de ferramentas do Microsoft Office InfoPath 2003 ou cria um novo modelo de formulário que funciona com o modelo de objeto compatível com o InfoPath 2003 (conforme descrito em [criar um modelo de formulário usando o objeto do InfoPath 2003 Modelo](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)), por padrão, o Microsoft InfoPath usará um subconjunto dos objetos e membros fornecidos pelo namespace [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) que sejam idênticos aos usados pelo InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="035be-105">When you add code to a form template that was created with the Microsoft Office InfoPath 2003 Toolkit or create a new form template that works with the InfoPath 2003-compatible object model (as described in [Create a Form Template Using the InfoPath 2003 Object Model](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)), by default, Microsoft InfoPath will use a subset of the objects and members provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace that are identical to those used by InfoPath 2003.</span></span> <span data-ttu-id="035be-106">Isso é feito para fornecer compatibilidade com o InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="035be-106">This is done to provide compatibility with InfoPath 2003.</span></span> <span data-ttu-id="035be-107">No enTanto, o modelo de objeto fornecido pelo namespace [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) inclui objetos e membros adicionais que oferecem novas funcionalidades que foram adicionadas ao Office InfoPath 2007 e ao InfoPath.</span><span class="sxs-lookup"><span data-stu-id="035be-107">However, the object model provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace includes additional objects and members that provide new functionality that was added to Office InfoPath 2007 and InfoPath.</span></span> 
  
<span data-ttu-id="035be-108">Por exemplo, o [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) permissionobject e as interfaces de [permissão](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) fornecem novas funcionalidades de gerenciamento de direitos de informação que não estão disponíveis no InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="035be-108">For example, the [PermissionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) and [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) interfaces provide new information rights management functionality that is not available in InfoPath 2003.</span></span> <span data-ttu-id="035be-109">Isso e outros novos objetos adicionados ao namespace Microsoft. Office. Interop. InfoPath. SemiTrust não estão disponíveis por padrão quando você abre ou cria um modelo de formulário de código gerenciado com o modelo de objeto compatível com o InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="035be-109">This, and other new objects added to the Microsoft.Office.Interop.InfoPath.SemiTrust namespace are not available by default when you open or create managed code form template with InfoPath 2003-compatible object model.</span></span> 
  
<span data-ttu-id="035be-110">Da mesma forma, enquanto a interface [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) fornece a mesma funcionalidade que o InfoPath 2003; a interface [_XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) foi versionada para incluir propriedades e métodos adicionais que foram adicionados no Office InfoPath 2007 e o [_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) foi versionado para incluir propriedades e métodos adicionais que foram adicionados ao InfoPath .</span><span class="sxs-lookup"><span data-stu-id="035be-110">Similarly, while the [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) interface provides the same functionality as InfoPath 2003; the [_XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) interface has been versioned to include additional properties and methods that were added in Office InfoPath 2007, and the [_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) has been versioned to include additional properties and methods that were added in InfoPath.</span></span> 
  
<span data-ttu-id="035be-111">Se você deseja usar objetos e membros que foram adicionados ao Office InfoPath 2007 ou InfoPath em um projeto de modelo de formulário criado usando o modelo de objeto fornecido pelo namespace **Microsoft. Office. Interop. InfoPath. SemiTrust** , você pode fazer isso, mas o código que usa esses membros não serão compatíveis com o InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="035be-111">If you want to use objects and members that were added in Office InfoPath 2007 or InfoPath in a form template project created using the object model provided by the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, you can do so, but code that uses these members will not be compatible with InfoPath 2003.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="035be-112">Todos os modelos de formulário com lógica de negócios criadas usando o modelo de objeto fornecido pelo namespace **Microsoft. Office. Interop. InfoPath. SemiTrust** , se eles usam objetos e membros compatíveis com o InfoPath ou não, não têm suporte para modelos de formulário habilitados para navegador implantados no Microsoft SharePoint Server 2010 com o InfoPath Forms Services.</span><span class="sxs-lookup"><span data-stu-id="035be-112">All form templates with business logic created using the object model provided by the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, whether they use objects and members compatible with InfoPath or not, are not supported for browser-enabled form templates deployed to Microsoft SharePoint Server 2010 with InfoPath Forms Services.</span></span> <span data-ttu-id="035be-113">A lógica de negócios para modelos de formulário habilitados para navegador deve usar o novo modelo de objeto de código gerenciado do InfoPath fornecido pelo namespace [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) .</span><span class="sxs-lookup"><span data-stu-id="035be-113">Business logic for browser-enabled form templates must use the new InfoPath managed code object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace.</span></span> 
  
## <a name="example"></a><span data-ttu-id="035be-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="035be-114">Example</span></span>

### <a name="creating-an-xdocument-or-application-object-variable-to-access-new-object-model-members"></a><span data-ttu-id="035be-115">Criar uma variável de objeto XDocument ou Application para acessar novos membros do modelo de objeto</span><span class="sxs-lookup"><span data-stu-id="035be-115">Creating an XDocument or Application Object Variable to Access New Object Model Members</span></span>

<span data-ttu-id="035be-116">Para acessar os novos objetos e membros que estão disponíveis no namespace **Microsoft. Office. Interop. InfoPath. SemiTrust** , você deve declarar e converter variáveis de objeto para a versão correta da interface que implementa esses membros.</span><span class="sxs-lookup"><span data-stu-id="035be-116">To access the new objects and members that are available in the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, you must declare and cast object variables to the correct version of the interface that implements these members.</span></span> <span data-ttu-id="035be-117">Por padrão, as `thisXDocument` variáveis `thisApplication` e acessam as versões compatíveis com o InfoPath 2003 das interfaces **_XDocument2** e [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) correspondentes.</span><span class="sxs-lookup"><span data-stu-id="035be-117">By default, the  `thisXDocument` and  `thisApplication` variables access the InfoPath 2003-compatible versions of the corresponding **_XDocument2** and [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) interfaces.</span></span> <span data-ttu-id="035be-118">Para acessar as interfaces do **_XDocument3** e do [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) que fornecem acesso a novas funcionalidades, você deve declarar uma variável de objeto do tipo **_XDocument3** ou **_Application3** e, em seguida, transmitir o objeto retornado pelo `thisXDocument`ou `thisApplication` variável para o mesmo tipo, conforme mostrado nos exemplos a seguir.</span><span class="sxs-lookup"><span data-stu-id="035be-118">To access the **_XDocument3** and [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) interfaces that provide access to new functionality, you must declare an object variable of the **_XDocument3** or **_Application3** type, and then cast the object returned by the  `thisXDocument` or  `thisApplication` variable to the same type as shown in the following examples.</span></span> 
  
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

### <a name="accessing-a-new-object-from-the-xdocument-or-application-object-variable-using-an-accessor-property"></a><span data-ttu-id="035be-119">Acessar um novo objeto da variável de objeto XDocument ou Application usando uma propriedade de assessor</span><span class="sxs-lookup"><span data-stu-id="035be-119">Accessing a New Object From The XDocument or Application Object Variable Using an Accessor Property</span></span>

<span data-ttu-id="035be-120">Depois de criar uma variável da versão mais recente _ **XDocument3** ou **_Application3** , você pode usá-la para acessar um objeto ou membro que forneça a nova funcionalidade do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="035be-120">After you have created a variable of the later version _ **XDocument3** or **_Application3** type, you can use it to access an object or member that provides new InfoPath functionality.</span></span> 
  
<span data-ttu-id="035be-121">O exemplo a seguir mostra como usar uma variável de objeto do tipo _ **XDocument3** com a propriedade de assessor [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) para acessar a nova interface de **permissão** e sua propriedade [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) para determinar se as configurações de permissão são habilitado para o formulário.</span><span class="sxs-lookup"><span data-stu-id="035be-121">The following example shows how to use an object variable of type _ **XDocument3** with the [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) accessor property to access the new **Permission** interface and its [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) property to determine if permission settings are enabled for the form.</span></span> 
  
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

### <a name="accessing-a-versioned-object-and-casting-to-the-versioned-type"></a><span data-ttu-id="035be-122">Acessar um objeto com controle de versão e uma projeção para o tipo de versão</span><span class="sxs-lookup"><span data-stu-id="035be-122">Accessing a Versioned Object and Casting to the Versioned Type</span></span>

<span data-ttu-id="035be-123">Se um objeto que existia no modelo de objeto do InfoPath 2003 tiver novas propriedades ou métodos adicionados a ele, o objeto que implementa esses novos membros terá um nome de versão.</span><span class="sxs-lookup"><span data-stu-id="035be-123">If an object that existed in the InfoPath 2003 object model has new properties or methods added to it, the object that implements those new members will have a name that is versioned.</span></span>
  
<span data-ttu-id="035be-124">Por exemplo, o objeto [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) não fornece acesso a duas novas propriedades que estão disponíveis somente ao usar o objeto [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) versionado: as propriedades [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) e [HideName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) .</span><span class="sxs-lookup"><span data-stu-id="035be-124">For example, the [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) object does not provide access to two new properties that are only available when using the versioned [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) object: the [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) and [HideName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) properties.</span></span> 
  
<span data-ttu-id="035be-125">Para acessar essas propriedades, você deve declarar uma variável de objeto do tipo **ViewInfo2** e converter o objeto retornado pela propriedade [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) da variável de objeto _ **XDocument3** para o tipo **ViewInfo2** conforme mostrado na seguinte como.</span><span class="sxs-lookup"><span data-stu-id="035be-125">To access these properties, you must declare an object variable of type **ViewInfo2** and cast the object returned by the [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) property of the _ **XDocument3** object variable to the **ViewInfo2** type as shown in the following example.</span></span> 
  
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


