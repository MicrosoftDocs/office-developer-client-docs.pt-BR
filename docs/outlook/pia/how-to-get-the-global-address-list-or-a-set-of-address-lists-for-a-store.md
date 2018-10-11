---
title: Identificar a lista de endereços global ou um conjunto de listas de endereços de um armazenamento
TOCTitle: Get the Global Address List or a set of address lists for a store
ms:assetid: a361ac58-25c6-4ce1-97b0-403ad67ee7a4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184631(v=office.15)
ms:contentKeyID: 55119800
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: b27c6c6fd9cf70a691f4a2df628a342cf024d8d6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406453"
---
# <a name="get-the-global-address-list-or-a-set-of-address-lists-for-a-store"></a><span data-ttu-id="5a8ef-102">Identificar a lista de endereços global ou um conjunto de listas de endereços de um armazenamento</span><span class="sxs-lookup"><span data-stu-id="5a8ef-102">Get the Global Address List or a set of address lists for a store</span></span>

<span data-ttu-id="5a8ef-103">Este tópico inclui dois exemplos de código que mostram como obter a lista de endereços Global (GAL) associada a um repositório e como obter todas as lista de endereços que estão associadas a um repositório.</span><span class="sxs-lookup"><span data-stu-id="5a8ef-103">This topic contains two code examples that show how to get the Global Address List (GAL) that is associated with a store, and how to get all of the address lists that are associated with a store.</span></span>

## <a name="example"></a><span data-ttu-id="5a8ef-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5a8ef-104">Example</span></span>

<span data-ttu-id="5a8ef-105">Em uma sessão do Outlook onde várias contas do Exchange são definidas no perfil de, pode contar várias listas de endereços associadas a um repositório.</span><span class="sxs-lookup"><span data-stu-id="5a8ef-105">In an Outlook session where multiple Exchange accounts are defined in the profile, there can be multiple address lists associated with a store.</span></span> <span data-ttu-id="5a8ef-106">Em cada um dos exemplos a seguir, o armazenamento específico de interesse é o armazenamento para a pasta atual exibida no explorer ativo, mas o algoritmo para obter uma lista de endereços Global ou um conjunto de objetos[AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) aplica-se de uma loja para qualquer repositório do Exchange.</span><span class="sxs-lookup"><span data-stu-id="5a8ef-106">In each of the following code examples, the specific store of interest is the store for the current folder displayed in the active explorer, but the algorithm to get a Global Address List or a set of [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) objects for a store applies to any Exchange store.</span></span>

<span data-ttu-id="5a8ef-107">O primeiro exemplo código contém o método DisplayGlobalAddressListForStore e a função GetGlobalAddressList.</span><span class="sxs-lookup"><span data-stu-id="5a8ef-107">The first code example contains the DisplayGlobalAddressListForStore method and the GetGlobalAddressList function.</span></span> <span data-ttu-id="5a8ef-108">O método DisplayGlobalAddressListForStore é exibido, na caixa de diálogo**selecionar nomes** a lista de endereços global que está associada ao repositório de dados atual.</span><span class="sxs-lookup"><span data-stu-id="5a8ef-108">The DisplayGlobalAddressListForStore method displays, in the **Select Names** dialog box, the Global Address List that is associated with the current store.</span></span> <span data-ttu-id="5a8ef-109">Primeiro, o DisplayGlobalAddressListForStore obtém o armazenamento atual.</span><span class="sxs-lookup"><span data-stu-id="5a8ef-109">DisplayGlobalAddressListForStore first obtains the current store.</span></span> <span data-ttu-id="5a8ef-110">Se o repositório de dados atual for um repositório do Exchange, GetGlobalAddressList é chamado para obter a lista de endereços Global associada ao repositório de dados atual.</span><span class="sxs-lookup"><span data-stu-id="5a8ef-110">If the current store is an Exchange store, GetGlobalAddressList is called to obtain the Global Address List associated with the current store.</span></span> 

<span data-ttu-id="5a8ef-111">GetGlobalAddressList usa o objeto[PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\))e a propriedade MAPI https://schemas.microsoft.com/mapi/proptag/0x3D150102 para obter a propriedade PR\_EMSMDB\_SECTION\_UID dO repositório de dados atual e de uma lista de endereços.</span><span class="sxs-lookup"><span data-stu-id="5a8ef-111">GetGlobalAddressList uses the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object and the MAPI property https://schemas.microsoft.com/mapi/proptag/0x3D150102 to obtain the PR\_EMSMDB\_SECTION\_UID property of an address list and the current store.</span></span> <span data-ttu-id="5a8ef-112">A GetGlobalAddressList identifica uma lista de endereços como associada a um repositório se as propriedades PR\_EMSMDB\_SECTION\_UID forem correspondentes e se a lista de endereços se a lista de endereços Global for a  [AddressListType](https://msdn.microsoft.com/library/bb610942\(v=office.15\)) e a propriedade [olExchangeGlobalAddressList](https://msdn.microsoft.com/library/bb644009\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="5a8ef-112">GetGlobalAddressList identifies an address list as associated with a store if their PR\_EMSMDB\_SECTION\_UID properties match, and the address list is the Global Address List if its [AddressListType](https://msdn.microsoft.com/library/bb610942\(v=office.15\)) property is [olExchangeGlobalAddressList](https://msdn.microsoft.com/library/bb644009\(v=office.15\)).</span></span> <span data-ttu-id="5a8ef-113">Se a chamada para a GetGlobalAddressList for concluída, a DisplayGlobalAddressListForStore usa o objeto[SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) para exibir a lista de endereços Global retornada na caixa de diálogo **selecionar nomes**.</span><span class="sxs-lookup"><span data-stu-id="5a8ef-113">If the call to GetGlobalAddressList succeeds, DisplayGlobalAddressListForStore uses the [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) object to display the returned Global Address List in the **Select Names** dialog box.</span></span>

<span data-ttu-id="5a8ef-114">Se você usar o Visual Studio para testar este exemplo de código, primeiro você deve adicionar uma referência para o componente de biblioteca de objetos do Microsoft Outlook 15.0 e especificar a variável Outlook quando você importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="5a8ef-114">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="5a8ef-115">A instrução**usando** não deve se situar antes de funções no exemplo de código mas deve ser adicionada antes da declaração classe pública.</span><span class="sxs-lookup"><span data-stu-id="5a8ef-115">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="5a8ef-116">A seguinte linha de código mostra como fazer a importação e de tarefa em C\#.</span><span class="sxs-lookup"><span data-stu-id="5a8ef-116">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
void DisplayGlobalAddressListForStore()
{
    Outlook.Folder currentFolder =
        Application.ActiveExplorer().CurrentFolder
        as Outlook.Folder;
    Outlook.Store currentStore = currentFolder.Store;
    if (currentStore.ExchangeStoreType !=
        Outlook.OlExchangeStoreType.olNotExchange)
    {
        Outlook.SelectNamesDialog snd = 
            Application.Session.GetSelectNamesDialog();
        Outlook.AddressList addrList = 
            GetGlobalAddressList(currentStore);
        if (addrList != null)
        {
            snd.InitialAddressList = addrList;
            snd.Display();
        }
    }
}

public Outlook.AddressList GetGlobalAddressList(Outlook.Store store)
{
    string  PR_EMSMDB_SECTION_UID = 
        @"https://schemas.microsoft.com/mapi/proptag/0x3D150102";
    if (store == null)
    {
        throw new ArgumentNullException();
    }
    Outlook.PropertyAccessor oPAStore = store.PropertyAccessor;
    string storeUID = oPAStore.BinaryToString(
        oPAStore.GetProperty(PR_EMSMDB_SECTION_UID));
    foreach (Outlook.AddressList addrList 
        in Application.Session.AddressLists)
    {
        Outlook.PropertyAccessor oPAAddrList = 
            addrList.PropertyAccessor;
        string addrListUID = oPAAddrList.BinaryToString(
            oPAAddrList.GetProperty(PR_EMSMDB_SECTION_UID));
        // Return addrList if match on storeUID
        // and type is olExchangeGlobalAddressList.
        if (addrListUID == storeUID && addrList.AddressListType ==
            Outlook.OlAddressListType.olExchangeGlobalAddressList)
        {
            return addrList;
        }
    }
    return null;
}
```

<span data-ttu-id="5a8ef-117">O segundo exemplo de código contém o método EnumerateAddressListsForStore e a função GetAddressLists.</span><span class="sxs-lookup"><span data-stu-id="5a8ef-117">The second code example contains the EnumerateAddressListsForStore method and GetAddressLists function.</span></span> <span data-ttu-id="5a8ef-118">O método EnumerateAddressListsForStore exibe a ordem de tipo e resolução de cada lista de endereços definida para o repositório de dados atual.</span><span class="sxs-lookup"><span data-stu-id="5a8ef-118">The EnumerateAddressListsForStore method displays the type and resolution order of each address list defined for the current store.</span></span> <span data-ttu-id="5a8ef-119">EnumerateAddressListsForStore primeiro obtém o armazenamento atual e liga a GetAddressLists para obter uma lista genérica do .NET Framework [do objeto\<T\> ](https://msdn.microsoft.com/pt-BR/library/6sh2ey19) que contém objetos AddressList para o armazenamento atual.</span><span class="sxs-lookup"><span data-stu-id="5a8ef-119">EnumerateAddressListsForStore first obtains the current store, and then calls GetAddressLists to obtain a .NET Framework generic [List\<T\>](https://msdn.microsoft.com/pt-BR/library/6sh2ey19) object that contains AddressList objects for the current store.</span></span> 

<span data-ttu-id="5a8ef-120">GetAddressLists enumera cada lista de endereços definida para a sessão, usa o objeto PropertyAccessor e a propriedade nomeada MAPI https://schemas.microsoft.com/mapi/proptag/0x3D150102 para obter a propriedade PR\_EMSMDB\_SECTION\_UID de uma lista de endereços e a propriedade PR\_EMSMDB\_SECTION\_de uma loja atual.</span><span class="sxs-lookup"><span data-stu-id="5a8ef-120">GetAddressLists enumerates each address list defined for the session, uses the PropertyAccessor object and the MAPI named property https://schemas.microsoft.com/mapi/proptag/0x3D150102 to obtain the PR\_EMSMDB\_SECTION\_UID property of an address list, and the PR\_EMSMDB\_SECTION\_UID property of a current store.</span></span> <span data-ttu-id="5a8ef-121">GetGlobalAddressList identifica uma lista de endereços como associada a um repositório se sua propriedade PR\_EMSMDB\_SECTION\_UID corresponder e retornar  um conjunto de lista de endereços para o armazenamento atual.</span><span class="sxs-lookup"><span data-stu-id="5a8ef-121">GetGlobalAddressList identifies an address list as associated with a store if their PR\_EMSMDB\_SECTION\_UID properties match, and returns a set of address lists for the current store.</span></span> <span data-ttu-id="5a8ef-122">EnumerateAddressListsForStore usa as propriedades [AddressListType](https://msdn.microsoft.com/library/bb610942\(v=office.15\)) e [ResolutionOrder](https://msdn.microsoft.com/library/bb646853\(v=office.15\)) do objeto **AddressList** para exibir o tipo e a resolução ordem para cada lista de endereços retornada.</span><span class="sxs-lookup"><span data-stu-id="5a8ef-122">EnumerateAddressListsForStore then uses the [AddressListType](https://msdn.microsoft.com/library/bb610942\(v=office.15\)) and [ResolutionOrder](https://msdn.microsoft.com/library/bb646853\(v=office.15\)) properties of the **AddressList** object to display the type and resolution order for each returned address list.</span></span>

```csharp
private void EnumerateAddressListsForStore()
{
    Outlook.Folder currentFolder =
        Application.ActiveExplorer().CurrentFolder
        as Outlook.Folder;
    Outlook.Store currentStore = currentFolder.Store;
    List<Outlook.AddressList> addrListsForStore = 
        GetAddressLists(currentStore);
    foreach (Outlook.AddressList addrList in addrListsForStore)
    {
        Debug.WriteLine(addrList.Name 
            + " " + addrList.AddressListType.ToString()
            + " Resolution Order: " +
            addrList.ResolutionOrder);
    }
}
public List<Outlook.AddressList> GetAddressLists(Outlook.Store store)
{
    List<Outlook.AddressList> addrLists = 
        new List<Microsoft.Office.Interop.Outlook.AddressList>();
    string PR_EMSMDB_SECTION_UID =
        @"https://schemas.microsoft.com/mapi/proptag/0x3D150102";
    if (store == null)
    {
        throw new ArgumentNullException();
    }
    Outlook.PropertyAccessor oPAStore = store.PropertyAccessor;
    string storeUID = oPAStore.BinaryToString(
        oPAStore.GetProperty(PR_EMSMDB_SECTION_UID));
    foreach (Outlook.AddressList addrList
        in Application.Session.AddressLists)
    {
        Outlook.PropertyAccessor oPAAddrList =
            addrList.PropertyAccessor;
        string addrListUID = oPAAddrList.BinaryToString(
            oPAAddrList.GetProperty(PR_EMSMDB_SECTION_UID));
        // Return addrList if match on storeUID
        // and type is olExchangeGlobalAddressList.
        if (addrListUID == storeUID)
        {
            addrLists.Add(addrList);
        }
    }
    return addrLists;
}
```

## <a name="see-also"></a><span data-ttu-id="5a8ef-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a8ef-123">See also</span></span>

- [<span data-ttu-id="5a8ef-124">Catálogo de Endereços</span><span class="sxs-lookup"><span data-stu-id="5a8ef-124">Address Book</span></span>](address-book.md)
