---
title: Objetos no Outlook PIA
TOCTitle: Objects in the Outlook PIA
ms:assetid: 1be732a6-d6da-4fa0-beaa-accf35db12d6
ms:mtpsurl: https://msdn.microsoft.com/library/Bb609459(v=office.15)
ms:contentKeyID: 55119778
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 772d857e10068871de16c2a3cd0528ab08088631
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270244"
---
# <a name="objects-in-the-outlook-pia"></a><span data-ttu-id="29c0f-102">Objetos no Outlook PIA</span><span class="sxs-lookup"><span data-stu-id="29c0f-102">Objects in the Outlook PIA</span></span>

<span data-ttu-id="29c0f-103">Enquanto estiver navegando no Outlook Primary Interop Assembly (PIA) em um pesquisador de objetos, você notará que muitas classes e interfaces têm nomes familiares, em referência à objetos no modelo de objeto do Outlook.</span><span class="sxs-lookup"><span data-stu-id="29c0f-103">When browsing the Outlook Primary Interop Assembly (PIA) in an object browser, you may notice that many interfaces and classes have names referencing familiar objects in the Outlook object model.</span></span> <span data-ttu-id="29c0f-104">Alguns objetos no modelo de objeto precisam ter um mapeamento individual nas interfaces no PIA.</span><span class="sxs-lookup"><span data-stu-id="29c0f-104">Some objects in the object model have a one-to-one mapping to interfaces in the PIA.</span></span> 

<span data-ttu-id="29c0f-105">Por exemplo, o **AddressEntry** está mapeado para a interface [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) e o objeto **AddressList** é mapeado para a interface [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\))no PIA.</span><span class="sxs-lookup"><span data-stu-id="29c0f-105">For example, the **AddressEntry** is mapped to the [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) interface and the **AddressList** object is mapped to the [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) interface in the PIA.</span></span> 

<span data-ttu-id="29c0f-106">No entanto, a maioria dos outros objetos têm um mapeamento de um para muitos no PIA.</span><span class="sxs-lookup"><span data-stu-id="29c0f-106">However, most other objects have a one-to-many mapping in the PIA.</span></span> <span data-ttu-id="29c0f-107">Este mapeamento de um para muitos é aplicado a todos os objetos adicionados a partir do Outlook 2007 e alguns objetos existentes antes do Microsoft Office Outlook 2007.</span><span class="sxs-lookup"><span data-stu-id="29c0f-107">This one-to-many mapping applies to some objects that existed before Microsoft Office Outlook 2007, and all objects added since Outlook 2007.</span></span> <span data-ttu-id="29c0f-108">Este tópico lista as interfaces, classes e delegados .NET que são mapeados para um objeto COM e descreve como acessar um objeto no PIA Outlook.</span><span class="sxs-lookup"><span data-stu-id="29c0f-108">This topic lists the typical .NET interfaces, classes, and delegates that are mapped to a COM object and describes how to access an object in the Outlook PIA.</span></span> <span data-ttu-id="29c0f-109">Ele também descreve algumas exceções no Outlook PIA onde os objetos estão ocultos ou preteridos no modelo de objeto com base em COM.</span><span class="sxs-lookup"><span data-stu-id="29c0f-109">It also describes a few exceptions in the Outlook PIA where the objects are hidden or deprecated in the COM-based object model.</span></span>

## <a name="helper-objects"></a><span data-ttu-id="29c0f-110">Objetos de ajuda</span><span class="sxs-lookup"><span data-stu-id="29c0f-110">Helper objects</span></span>

<span data-ttu-id="29c0f-111">Esta seção ilustra as típicas classes auxiliares de um objeto no Outlook PIA usando o objeto **FormRegion** como um exemplo.</span><span class="sxs-lookup"><span data-stu-id="29c0f-111">This section illustrates the typical helper classes for an object in the Outlook PIA by using the **FormRegion** object as an example.</span></span> <span data-ttu-id="29c0f-112">O objeto **FormRegion** foi adicionado ao modelo de objeto do Outlook 2007.</span><span class="sxs-lookup"><span data-stu-id="29c0f-112">The **FormRegion** object was added to the object model in Outlook 2007.</span></span> <span data-ttu-id="29c0f-113">Relacionados para o objeto **FormRegion** no PIA são representantes ilustrados na Figura 1, interfaces e classes.</span><span class="sxs-lookup"><span data-stu-id="29c0f-113">Related to the **FormRegion** object in the PIA are the interfaces, classes, and delegates, illustrated in Figure 1.</span></span>

<span data-ttu-id="29c0f-114">**Figura 1. O objeto FormRegion representado no modelo de objeto do Outlook e no PIA Outlook**</span><span class="sxs-lookup"><span data-stu-id="29c0f-114">**Figure 1. The FormRegion object represented in the Outlook object model and in the Outlook PIA**</span></span>

![O objeto FormRegion representado no modelo de objeto do Outlook e no PIA Outlook](media/pia-outlook-object-model.gif)

<span data-ttu-id="29c0f-116">Uma interface que você pode acessar com mais frequência é o **FormRegion** e os membros de método, propriedade e evento do objeto é a interface [FormRegion](https://msdn.microsoft.com/library/bb652633\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="29c0f-116">The one interface that you most often use to access the **FormRegion** object and its method, property, and event members is the [FormRegion](https://msdn.microsoft.com/library/bb652633\(v=office.15\)) interface.</span></span> <span data-ttu-id="29c0f-117">No entanto, você não deve considerar a interface **FormRegion** .NET como uma imagem espelhada exata do objeto **FormRegion** COM; se examinar o Pesquisador de Objetos no Visual Studio, você descobrirá que a interface **FormRegion** é herdada de outra interface, a interface [ \_FormRegion](https://msdn.microsoft.com/library/bb645761\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="29c0f-117">However, you should not consider the **FormRegion** .NET interface as an exact mirror image of the **FormRegion** COM object; if you look at the Object Browser in Visual Studio, you will find that the **FormRegion** interface inherits from another interface, the [\_FormRegion](https://msdn.microsoft.com/library/bb645761\(v=office.15\)) interface.</span></span> <span data-ttu-id="29c0f-118">Na verdade, a interface **FormRegion** é apenas uma das seguintes interfaces e classes que resultam da criação do PIA Outlook baseiam-se a biblioteca COM.</span><span class="sxs-lookup"><span data-stu-id="29c0f-118">In fact, the **FormRegion** interface is just one of the few interfaces and classes that result from creating the Outlook PIA based on the COM type library.</span></span>

<span data-ttu-id="29c0f-119">Para criar o Outlook PIA, o Outlook usa o Importador de Bibliotecas de Tipos (TLBIMP) no .NET Framework para converter definições de tipos da biblioteca de tipos COM em definições equivalentes em um assembly de tempo de execução em linguagem comum.</span><span class="sxs-lookup"><span data-stu-id="29c0f-119">To create the Outlook PIA, Outlook uses the Type Library Importer (TLBIMP) in the .NET Framework to convert type definitions in the COM type library into equivalent definitions in a Common Language Runtime assembly.</span></span> <span data-ttu-id="29c0f-120">Na COM, o objeto **FormRegion** é realmente um coclass que consiste em duas interfaces a seguir, definindo as interfaces que o objeto **FormRegion** implementa:</span><span class="sxs-lookup"><span data-stu-id="29c0f-120">In COM, the **FormRegion** object is actually a coclass that consists of the following two interfaces defining the interfaces that the **FormRegion** object implements:</span></span>

- <span data-ttu-id="29c0f-121">A interface principal **\_FormRegion**</span><span class="sxs-lookup"><span data-stu-id="29c0f-121">The primary interface **\_FormRegion**</span></span>

- <span data-ttu-id="29c0f-122">A interface do evento [FormRegionEvents](https://msdn.microsoft.com/library/bb611940\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="29c0f-122">The event interface [FormRegionEvents](https://msdn.microsoft.com/library/bb611940\(v=office.15\))</span></span>

<span data-ttu-id="29c0f-123">TLBIMP diretamente importa **\_FormRegion** e **FormRegionEvents** da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="29c0f-123">TLBIMP directly imports **\_FormRegion** and **FormRegionEvents** from the type library.</span></span>

<span data-ttu-id="29c0f-124">Além de importar a interface principal e a interface do evento, o TLBIMP cria uma interface .NET com o mesmo nome de objeto COM e uma classe .NET que usa o nome do objeto e acrescentado de "Classe".</span><span class="sxs-lookup"><span data-stu-id="29c0f-124">Other than importing the primary interface and event interface, TLBIMP creates a .NET interface that has the same name as the COM object, and a .NET class that uses the name of the object and appends it with "Class".</span></span> <span data-ttu-id="29c0f-125">No caso do objeto **FormRegion**, o TLBIMP cria o seguinte:</span><span class="sxs-lookup"><span data-stu-id="29c0f-125">In the case of the **FormRegion** object, TLBIMP creates the following:</span></span>

- <span data-ttu-id="29c0f-126">A interface do .NET **FormRegion**</span><span class="sxs-lookup"><span data-stu-id="29c0f-126">The .NET interface **FormRegion**</span></span>

- <span data-ttu-id="29c0f-127">A classe .NET [FormRegionClass](https://msdn.microsoft.com/library/bb624204\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="29c0f-127">The .NET class [FormRegionClass](https://msdn.microsoft.com/library/bb624204\(v=office.15\))</span></span>

<span data-ttu-id="29c0f-128">A partir das interfaces .NET e classe .NET mencionadas neste tópico, você sempre pode usar a interface .NET que o TLBIMP cria para acessar um objeto.</span><span class="sxs-lookup"><span data-stu-id="29c0f-128">Of the .NET interfaces and .NET class mentioned in this topic, you always use the .NET interface that TLBIMP creates to access an object.</span></span> <span data-ttu-id="29c0f-129">Por exemplo, para acessar um objeto **FormRegion** em VB, você sempre pode usar a interface **FormRegion**, como no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="29c0f-129">For example, to access a **FormRegion** object in VB, you always use the **FormRegion** interface, as in the following code example:</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
Sub DemoFormRegion(ByVal Region As Outlook.FormRegion)
    Dim MyFormRegion As Outlook.FormRegion = Region
    ' Additional method code here
End Sub
```

<br/>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook; 
void DemoFormRegion(Outlook.FormRegion region) 
{
    Outlook.FormRegion myFormRegion = region; 
    // Additional method code here
}
```

<span data-ttu-id="29c0f-130">Para informações sobre a finalidade da interface principal e da classe .NET que o TLBIMP importa e cria respectivamente, confira [métodos e propriedades no PIA Outlook](methods-and-properties-in-the-outlook-pia.md).</span><span class="sxs-lookup"><span data-stu-id="29c0f-130">For information about the purpose of the primary interface and the .NET class that TLBIMP imports and creates respectively, see [Methods and properties in the Outlook PIA](methods-and-properties-in-the-outlook-pia.md).</span></span> <span data-ttu-id="29c0f-131">Para informações sobre a finalidade de interfaces relacionadas a eventos, representantes e classes de sink helper, confira[eventos no PIA Outlook](events-in-the-outlook-pia.md).</span><span class="sxs-lookup"><span data-stu-id="29c0f-131">For information about the purpose of the event-related interfaces, delegates, and sink helper classes, see [Events in the Outlook PIA](events-in-the-outlook-pia.md).</span></span>

## <a name="deprecated-objects"></a><span data-ttu-id="29c0f-132">Objetos preteridos</span><span class="sxs-lookup"><span data-stu-id="29c0f-132">Deprecated objects</span></span>

<span data-ttu-id="29c0f-133">Objetos substituídos na biblioteca de tipos de objetos são expostos no PIA Outlook.</span><span class="sxs-lookup"><span data-stu-id="29c0f-133">Objects deprecated in the type library are exposed in the Outlook PIA.</span></span> <span data-ttu-id="29c0f-134">Por exemplo, os objetos **\_DDocSiteControl** e **\_DRecipientControl** estão ocultos na biblioteca de tipos, mas exibidos no PIA.</span><span class="sxs-lookup"><span data-stu-id="29c0f-134">For example, the **\_DDocSiteControl** and **\_DRecipientControl** objects are hidden in the type library but are exposed in the PIA.</span></span>

<span data-ttu-id="29c0f-135">Outro exemplo de um objeto obsoletos é o objeto **MAPIFolder**.</span><span class="sxs-lookup"><span data-stu-id="29c0f-135">Another example of a deprecated object is the **MAPIFolder** object.</span></span> <span data-ttu-id="29c0f-136">Iniciando no Outlook 2007,a **pasta** objeto substituiu o objeto **MAPIFolder** no modelo de objeto.</span><span class="sxs-lookup"><span data-stu-id="29c0f-136">Starting in Outlook 2007, the **Folder** object has replaced the **MAPIFolder** object in the object model.</span></span> <span data-ttu-id="29c0f-137">Soluções existentes devem substituir as referências a **MAPIFolder** pela **pasta**, e todas as soluções de novas a partir do Outlook 2007 devem usar somente o objeto **pasta**.</span><span class="sxs-lookup"><span data-stu-id="29c0f-137">Existing solutions should replace references to **MAPIFolder** by **Folder**, and all solutions new for Outlook 2007 and after should use only the **Folder** object.</span></span> <span data-ttu-id="29c0f-138">Para obter soluções não gerenciadas, pesquisador de objetos do Editor do Visual Basic não lista os objetos **MAPIFolder** nem como um objeto oculto.</span><span class="sxs-lookup"><span data-stu-id="29c0f-138">For unmanaged solutions, the Object Browser of the Visual Basic Editor no longer lists the **MAPIFolder** object, not even as a hidden object.</span></span> 

<span data-ttu-id="29c0f-139">Para obter soluções gerenciadas, mesmo que o Outlook PIA exponha uma interface de [pasta](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) na qual você possa acessar o objeto **pasta** e seus membros, o Outlook PIA também expõe o [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) como uma interface que define os membros do **objeto** pasta.</span><span class="sxs-lookup"><span data-stu-id="29c0f-139">For managed solutions, even though the Outlook PIA exposes a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) interface through which you access the **Folder** object and its members, the Outlook PIA also exposes [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) as an interface that defines the members of the **Folder** object.</span></span>

## <a name="see-also"></a><span data-ttu-id="29c0f-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="29c0f-140">See also</span></span>

- [<span data-ttu-id="29c0f-141">Relacionando o PIA Outlook com o modelo de objeto</span><span class="sxs-lookup"><span data-stu-id="29c0f-141">Relating the Outlook PIA with the object model</span></span>](relating-the-outlook-pia-with-the-object-model.md)


