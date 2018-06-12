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
# <a name="use-microsoftofficeinteropinfopathsemitrust-members-not-compatible-with-infopath"></a><span data-ttu-id="88741-104">Use SemiTrust membros não é compatíveis com o InfoPath</span><span class="sxs-lookup"><span data-stu-id="88741-104">Use Microsoft.Office.Interop.InfoPath.SemiTrust members not compatible with InfoPath</span></span>

<span data-ttu-id="88741-105">Quando você adicionar código para um modelo de formulário foi criado com o Microsoft Office InfoPath 2003 Toolkit ou cria um novo modelo de formulário que funciona com o modelo de objeto compatível com o InfoPath 2003 (conforme descrito na [criar um modelo de formulário usando o objeto do InfoPath 2003 Modelo](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)), por padrão, o Microsoft InfoPath usará um subconjunto dos objetos e membros fornecidos pelo namespace [SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) que são idênticas às usadas pelo InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="88741-105">When you add code to a form template that was created with the Microsoft Office InfoPath 2003 Toolkit or create a new form template that works with the InfoPath 2003-compatible object model (as described in [Create a Form Template Using the InfoPath 2003 Object Model](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)), by default, Microsoft InfoPath will use a subset of the objects and members provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace that are identical to those used by InfoPath 2003.</span></span> <span data-ttu-id="88741-106">Isso é feito para fornecer compatibilidade com o InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="88741-106">This is done to provide compatibility with InfoPath 2003.</span></span> <span data-ttu-id="88741-107">No entanto, o modelo de objeto fornecido pelo namespace [SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) inclui objetos adicionais e os membros que fornecem a nova funcionalidade que foi adicionada ao Office InfoPath 2007 e InfoPath.</span><span class="sxs-lookup"><span data-stu-id="88741-107">However, the object model provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace includes additional objects and members that provide new functionality that was added to Office InfoPath 2007 and InfoPath.</span></span> 
  
<span data-ttu-id="88741-108">Por exemplo, as interfaces de [permissão](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) e [PermissionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) fornecem a nova funcionalidade de gerenciamento de direitos de informação que não está disponível no InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="88741-108">For example, the [PermissionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) and [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) interfaces provide new information rights management functionality that is not available in InfoPath 2003.</span></span> <span data-ttu-id="88741-109">Este e outros novos objetos adicionados ao namespace SemiTrust não estão disponíveis por padrão quando você abre ou cria um modelo de formulário de código gerenciado com o modelo de objeto compatível com o InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="88741-109">This, and other new objects added to the Microsoft.Office.Interop.InfoPath.SemiTrust namespace are not available by default when you open or create managed code form template with InfoPath 2003-compatible object model.</span></span> 
  
<span data-ttu-id="88741-110">Da mesma forma, enquanto o [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) interface oferece a mesma funcionalidade que o InfoPath 2003; a interface de [_XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) foi versionada para incluir propriedades e métodos que foram adicionados no Office InfoPath 2007 adicionais e o [_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) ficou versionado para incluir propriedades e métodos que foram adicionados no InfoPath adicionais .</span><span class="sxs-lookup"><span data-stu-id="88741-110">Similarly, while the [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) interface provides the same functionality as InfoPath 2003; the [_XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) interface has been versioned to include additional properties and methods that were added in Office InfoPath 2007, and the [_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) has been versioned to include additional properties and methods that were added in InfoPath.</span></span> 
  
<span data-ttu-id="88741-111">Se você deseja usar objetos e membros que foram adicionados no Office InfoPath 2007 ou InfoPath em um projeto de modelo de formulário criado usando o modelo de objeto fornecido pelo namespace **SemiTrust** , você poderá fazer isso, mas o código que usa Esses membros não será compatíveis com o InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="88741-111">If you want to use objects and members that were added in Office InfoPath 2007 or InfoPath in a form template project created using the object model provided by the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, you can do so, but code that uses these members will not be compatible with InfoPath 2003.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="88741-112">Todos os modelos de formulário com lógica de negócios criados usando o modelo de objeto fornecido pelo namespace **SemiTrust** , se eles usam objetos e membros compatíveis com o InfoPath ou não, não há suporte para modelos de formulário habilitados para navegador implantados para Microsoft SharePoint Server 2010 com o InfoPath Forms Services.</span><span class="sxs-lookup"><span data-stu-id="88741-112">All form templates with business logic created using the object model provided by the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, whether they use objects and members compatible with InfoPath or not, are not supported for browser-enabled form templates deployed to Microsoft SharePoint Server 2010 with InfoPath Forms Services.</span></span> <span data-ttu-id="88741-113">A lógica de negócios para modelos de formulário habilitados para navegador deve usar o novo modelo de objeto de código gerenciado do InfoPath fornecido pelo namespace [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) .</span><span class="sxs-lookup"><span data-stu-id="88741-113">Business logic for browser-enabled form templates must use the new InfoPath managed code object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace.</span></span> 
  
## <a name="example"></a><span data-ttu-id="88741-114">Example</span><span class="sxs-lookup"><span data-stu-id="88741-114">Example</span></span>

### <a name="creating-an-xdocument-or-application-object-variable-to-access-new-object-model-members"></a><span data-ttu-id="88741-115">Criando um XDocument ou a variável de objeto de aplicativo para o Access novos membros do modelo de objeto</span><span class="sxs-lookup"><span data-stu-id="88741-115">Creating an XDocument or Application Object Variable to Access New Object Model Members</span></span>

<span data-ttu-id="88741-116">Para acessar os novos objetos e membros que estão disponíveis no namespace **SemiTrust** , você deve declarar e convertida de variáveis de objeto para a versão correta da interface que implementa esses membros.</span><span class="sxs-lookup"><span data-stu-id="88741-116">To access the new objects and members that are available in the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, you must declare and cast object variables to the correct version of the interface that implements these members.</span></span> <span data-ttu-id="88741-117">Por padrão, o `thisXDocument` e `thisApplication` variáveis acessar as versões compatíveis com o InfoPath 2003 do correspondente **_XDocument2** e interfaces [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) .</span><span class="sxs-lookup"><span data-stu-id="88741-117">By default, the  `thisXDocument` and  `thisApplication` variables access the InfoPath 2003-compatible versions of the corresponding **_XDocument2** and [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) interfaces.</span></span> <span data-ttu-id="88741-118">Para acessar as interfaces **_XDocument3** e [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) que fornecem acesso a nova funcionalidade, você deve declarar uma variável de objeto do tipo **_XDocument3** ou **_Application3** e difundir o objeto retornado pelo `thisXDocument`ou `thisApplication` variável para o mesmo tipo, conforme mostrado nos exemplos a seguir.</span><span class="sxs-lookup"><span data-stu-id="88741-118">To access the **_XDocument3** and [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) interfaces that provide access to new functionality, you must declare an object variable of the **_XDocument3** or **_Application3** type, and then cast the object returned by the  `thisXDocument` or  `thisApplication` variable to the same type as shown in the following examples.</span></span> 
  
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

### <a name="accessing-a-new-object-from-the-xdocument-or-application-object-variable-using-an-accessor-property"></a><span data-ttu-id="88741-119">Acessando um novo objeto na variável de objeto de aplicativo, usando uma propriedade de acessador ou XDocument</span><span class="sxs-lookup"><span data-stu-id="88741-119">Accessing a New Object From The XDocument or Application Object Variable Using an Accessor Property</span></span>

<span data-ttu-id="88741-120">Depois de criar uma variável do _ versão posterior **XDocument3** ou tipo de **_Application3** , você pode usá-lo para acessar um objeto ou membro que fornece a nova funcionalidade do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="88741-120">After you have created a variable of the later version _ **XDocument3** or **_Application3** type, you can use it to access an object or member that provides new InfoPath functionality.</span></span> 
  
<span data-ttu-id="88741-121">O exemplo a seguir mostra como usar uma variável de objeto do tipo _ **XDocument3** com a propriedade de acessador de [permissão](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) para acessar a nova interface de **permissão** e sua propriedade [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) para determinar se as configurações de permissão são habilitado para o formulário.</span><span class="sxs-lookup"><span data-stu-id="88741-121">The following example shows how to use an object variable of type _ **XDocument3** with the [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) accessor property to access the new **Permission** interface and its [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) property to determine if permission settings are enabled for the form.</span></span> 
  
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

### <a name="accessing-a-versioned-object-and-casting-to-the-versioned-type"></a><span data-ttu-id="88741-122">Acessando um objeto versionado e projeção para o tipo de versionado</span><span class="sxs-lookup"><span data-stu-id="88741-122">Accessing a Versioned Object and Casting to the Versioned Type</span></span>

<span data-ttu-id="88741-123">Se um objeto que existia no modelo de objeto do InfoPath 2003 tiver novas propriedades ou métodos adicionados a ela, o objeto que implementa esses novos membros terá um nome que for atualizado.</span><span class="sxs-lookup"><span data-stu-id="88741-123">If an object that existed in the InfoPath 2003 object model has new properties or methods added to it, the object that implements those new members will have a name that is versioned.</span></span>
  
<span data-ttu-id="88741-124">Por exemplo, o objeto [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) não fornece acesso a duas novas propriedades que só estão disponíveis ao usar o objeto de [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) versionado: as propriedades [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) e [HideName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) .</span><span class="sxs-lookup"><span data-stu-id="88741-124">For example, the [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) object does not provide access to two new properties that are only available when using the versioned [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) object: the [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) and [HideName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) properties.</span></span> 
  
<span data-ttu-id="88741-125">Para acessar essas propriedades, você deve declarar uma variável de objeto do tipo **ViewInfo2** e converter o objeto retornado pela propriedade [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) da variável de objeto _ **XDocument3** para o tipo de **ViewInfo2** , conforme mostrado no seguinte exemplo.</span><span class="sxs-lookup"><span data-stu-id="88741-125">To access these properties, you must declare an object variable of type **ViewInfo2** and cast the object returned by the [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) property of the _ **XDocument3** object variable to the **ViewInfo2** type as shown in the following example.</span></span> 
  
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


