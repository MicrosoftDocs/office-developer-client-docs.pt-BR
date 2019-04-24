---
title: Identificar a lista de endereços global ou um conjunto de listas de endereços de um armazenamento
TOCTitle: Get the Global Address List or a set of address lists for a store
ms:assetid: a361ac58-25c6-4ce1-97b0-403ad67ee7a4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184631(v=office.15)
ms:contentKeyID: 55119800
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 582b0e836edc361d1d8717f94a5d7490c57cd530
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320115"
---
# <a name="get-the-global-address-list-or-a-set-of-address-lists-for-a-store"></a>Identificar a lista de endereços global ou um conjunto de listas de endereços de um armazenamento

Este tópico inclui dois exemplos de código que mostram como obter a lista de endereços Global (GAL) associada a um repositório e como obter todas as lista de endereços que estão associadas a um repositório.

## <a name="example"></a>Exemplo

Em uma sessão do Outlook onde várias contas do Exchange são definidas no perfil de, pode contar várias listas de endereços associadas a um repositório. Em cada um dos exemplos a seguir, o armazenamento específico de interesse é o armazenamento para a pasta atual exibida no explorer ativo, mas o algoritmo para obter uma lista de endereços Global ou um conjunto de objetos[AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) aplica-se de uma loja para qualquer repositório do Exchange.

O primeiro exemplo código contém o método DisplayGlobalAddressListForStore e a função GetGlobalAddressList. O método DisplayGlobalAddressListForStore é exibido, na caixa de diálogo**selecionar nomes** a lista de endereços global que está associada ao repositório de dados atual. Primeiro, o DisplayGlobalAddressListForStore obtém o armazenamento atual. Se o repositório de dados atual for um repositório do Exchange, GetGlobalAddressList é chamado para obter a lista de endereços Global associada ao repositório de dados atual. 

GetGlobalAddressList usa o objeto[PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\))e a propriedade MAPI https://schemas.microsoft.com/mapi/proptag/0x3D150102 para obter a propriedade PR\_EMSMDB\_SECTION\_UID dO repositório de dados atual e de uma lista de endereços. A GetGlobalAddressList identifica uma lista de endereços como associada a um repositório se as propriedades PR\_EMSMDB\_SECTION\_UID forem correspondentes e se a lista de endereços se a lista de endereços Global for a  [AddressListType](https://msdn.microsoft.com/library/bb610942\(v=office.15\)) e a propriedade [olExchangeGlobalAddressList](https://msdn.microsoft.com/library/bb644009\(v=office.15\)). Se a chamada para a GetGlobalAddressList for concluída, a DisplayGlobalAddressListForStore usa o objeto[SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) para exibir a lista de endereços Global retornada na caixa de diálogo **selecionar nomes**.

Se você usar o Visual Studio para testar este exemplo de código, primeiro você deve adicionar uma referência para o componente de biblioteca de objetos do Microsoft Outlook 15.0 e especificar a variável Outlook quando você importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A seguinte linha de código mostra como fazer a importação e de tarefa em C\#.

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

O segundo exemplo de código contém o método EnumerateAddressListsForStore e a função GetAddressLists. O método EnumerateAddressListsForStore exibe a ordem de tipo e resolução de cada lista de endereços definida para o repositório de dados atual. EnumerateAddressListsForStore primeiro obtém o armazenamento atual e liga a GetAddressLists para obter uma lista genérica do .NET Framework [do objeto\<T\> ](https://msdn.microsoft.com/en-us/library/6sh2ey19) que contém objetos AddressList para o armazenamento atual. 

GetAddressLists enumera cada lista de endereços definida para a sessão, usa o objeto PropertyAccessor e a propriedade nomeada MAPI https://schemas.microsoft.com/mapi/proptag/0x3D150102 para obter a propriedade PR\_EMSMDB\_SECTION\_UID de uma lista de endereços e a propriedade PR\_EMSMDB\_SECTION\_de uma loja atual. GetGlobalAddressList identifica uma lista de endereços como associada a um repositório se sua propriedade PR\_EMSMDB\_SECTION\_UID corresponder e retornar  um conjunto de lista de endereços para o armazenamento atual. EnumerateAddressListsForStore usa as propriedades [AddressListType](https://msdn.microsoft.com/library/bb610942\(v=office.15\)) e [ResolutionOrder](https://msdn.microsoft.com/library/bb646853\(v=office.15\)) do objeto **AddressList** para exibir o tipo e a resolução ordem para cada lista de endereços retornada.

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

## <a name="see-also"></a>Confira também

- [Catálogo de Endereços](address-book.md)

