---
title: Criar uma lista de distribuição
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b63a6024-910d-4569-a3b4-c3ebf0b32c3d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7108ae215562169244100a56cc9b9208d78b1893
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424172"
---
# <a name="creating-a-distribution-list"></a><span data-ttu-id="8e579-103">Criar uma lista de distribuição</span><span class="sxs-lookup"><span data-stu-id="8e579-103">Creating a distribution list</span></span>

<span data-ttu-id="8e579-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e579-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e579-105">Os clientes podem criar uma lista de distribuição diretamente em um contêiner modificável, como o catálogo de endereços pessoal (PAB).</span><span class="sxs-lookup"><span data-stu-id="8e579-105">Clients can create a distribution list directly into a modifiable container such as the personal address book (PAB).</span></span>
  
<span data-ttu-id="8e579-106">**Para criar uma lista de distribuição no PAB**</span><span class="sxs-lookup"><span data-stu-id="8e579-106">**To create a distribution list in the PAB**</span></span>
  
1. <span data-ttu-id="8e579-107">Crie uma matriz de marca de propriedade dimensionada com uma marca de propriedade, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="8e579-107">Create a sized property tag array with one property tag, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), as follows:</span></span>
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. <span data-ttu-id="8e579-108">Chame [IAddrBook:: GetPAB](iaddrbook-getpab.md) para recuperar o identificador de entrada do PAB.</span><span class="sxs-lookup"><span data-stu-id="8e579-108">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> <span data-ttu-id="8e579-109">Se houver um erro ou **GetPAB** retornar zero ou nulo, não continue.</span><span class="sxs-lookup"><span data-stu-id="8e579-109">If there is an error or **GetPAB** returns zero or NULL, do not continue.</span></span> 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. <span data-ttu-id="8e579-110">Chame [IAddrBook:: OpenEntry](iaddrbook-openentry.md) para abrir o PAB.</span><span class="sxs-lookup"><span data-stu-id="8e579-110">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the PAB.</span></span> <span data-ttu-id="8e579-111">O parâmetro de saída _ulObjType_ deve ser definido como MAPI_ABCONT.</span><span class="sxs-lookup"><span data-stu-id="8e579-111">The  _ulObjType_ output parameter should be set to MAPI_ABCONT.</span></span> 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. <span data-ttu-id="8e579-112">Chame o método [IMAPIProp::](imapiprop-getprops.md) GetProps do PAB para recuperar a propriedade PR_DEF_CREATE_DL, o modelo que ele usa para criar uma lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="8e579-112">Call the PAB's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the PR_DEF_CREATE_DL property, the template that it uses to create a distribution list.</span></span> 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. <span data-ttu-id="8e579-113">Se \*\*\*\* GetProps falhar:</span><span class="sxs-lookup"><span data-stu-id="8e579-113">If **GetProps** fails:</span></span> 
    
   1. <span data-ttu-id="8e579-114">Chame o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) do PAB para abrir a propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) com a \*\*\*\* interface IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="8e579-114">Call the PAB's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> 
      
   2. <span data-ttu-id="8e579-115">Crie uma restrição de propriedade para pesquisar a linha com a coluna **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) igual a "MAPIPDL".</span><span class="sxs-lookup"><span data-stu-id="8e579-115">Create a property restriction to search for the row with the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column equal to "MAPIPDL."</span></span> 
      
   3. <span data-ttu-id="8e579-116">Call [IMAPITable:: FindRow](imapitable-findrow.md) para localizar esta linha.</span><span class="sxs-lookup"><span data-stu-id="8e579-116">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate this row.</span></span> 
    
6. <span data-ttu-id="8e579-117">Salve o identificador de entrada retornado por \*\*\*\* GetProps ou **FindRow**.</span><span class="sxs-lookup"><span data-stu-id="8e579-117">Save the entry identifier returned by either **GetProps** or **FindRow**.</span></span>
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. <span data-ttu-id="8e579-118">Chame o método [IABContainer:: createentry](iabcontainer-createentry.md) do PAB para criar uma nova entrada usando o modelo representado pelo identificador de entrada salvo.</span><span class="sxs-lookup"><span data-stu-id="8e579-118">Call the PAB's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new entry using the template represented by the saved entry identifier.</span></span> <span data-ttu-id="8e579-119">Não presuma que o objeto retornado será uma lista de distribuição, em vez de um usuário de mensagens, quando esta chamada for remota.</span><span class="sxs-lookup"><span data-stu-id="8e579-119">Do not assume that the object returned will be a distribution list rather than a messaging user when this call is remoted.</span></span> <span data-ttu-id="8e579-120">Observe que o sinalizador CREATE_CHECK_DUP é passado no parâmetro _parâmetroulflags_ para impedir que a entrada seja adicionada duas vezes.</span><span class="sxs-lookup"><span data-stu-id="8e579-120">Notice that the CREATE_CHECK_DUP flag is passed in the  _ulFlags_ parameter to prevent the entry from being added twice.</span></span> 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. <span data-ttu-id="8e579-121">Chame o método **IUnknown:: QueryInterface** da nova entrada, passando IID_IDistList como o identificador de interface, para determinar se a entrada é uma lista de distribuição e oferece suporte à interface [IDistList: IMAPIContainer](idistlistimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="8e579-121">Call the new entry's **IUnknown::QueryInterface** method, passing IID_IDistList as the interface identifier, to determine if the entry is a distribution list and supports the [IDistList : IMAPIContainer](idistlistimapicontainer.md) interface.</span></span> <span data-ttu-id="8e579-122">Como **createentry** retorna um ponteiro **IMAPIProp** em vez do ponteiro do **IMailUser** ou do **IDistList** mais específico, verifique se um objeto de lista de distribuição foi criado.</span><span class="sxs-lookup"><span data-stu-id="8e579-122">Because **CreateEntry** returns an **IMAPIProp** pointer rather than the more specific **IMailUser** or **IDistList** pointer, check that a distribution list object was created.</span></span> <span data-ttu-id="8e579-123">Se a **QueryInterface** for bem-sucedida, você poderá ter certeza de que criou uma lista de distribuição em vez de um usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="8e579-123">If **QueryInterface** succeeds, you can be sure that you have created a distribution list rather than a messaging user.</span></span> 
    
9. <span data-ttu-id="8e579-124">Chame o método [IMAPIProp::](imapiprop-setprops.md) SetProps da lista de distribuição para definir seu nome para exibição e outras propriedades.</span><span class="sxs-lookup"><span data-stu-id="8e579-124">Call the distribution list's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set its display name and other properties.</span></span> 
    
10. <span data-ttu-id="8e579-125">Chame o método [IABContainer:: createentry](iabcontainer-createentry.md) da lista de distribuição para adicionar um ou mais usuários de mensagens.</span><span class="sxs-lookup"><span data-stu-id="8e579-125">Call the distribution list's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to add one or more messaging users.</span></span> 
    
11. <span data-ttu-id="8e579-126">Chame o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) da lista de distribuição quando estiver pronto para salvá-lo.</span><span class="sxs-lookup"><span data-stu-id="8e579-126">Call the distribution list's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method when you're ready to save it.</span></span> <span data-ttu-id="8e579-127">Para recuperar o identificador de entrada da lista de distribuição salva, defina o sinalizador KEEP_OPEN_READWRITE e, em seguida, chame [IMAPIProp::](imapiprop-getprops.md) GetProps solicitando a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8e579-127">To retrieve the entry identifier of the saved distribution list, set the KEEP_OPEN_READWRITE flag and then call [IMAPIProp::GetProps](imapiprop-getprops.md) requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
12. <span data-ttu-id="8e579-128">Libere a nova lista de distribuição e o PAB chamando seus métodos **IUnknown:: Release** .</span><span class="sxs-lookup"><span data-stu-id="8e579-128">Release the new distribution list and the PAB by calling their **IUnknown::Release** methods.</span></span> 
    
13. <span data-ttu-id="8e579-129">Chame [MAPIFreeBuffer](mapifreebuffer.md) para liberar a memória para o identificador de entrada do PAB e a matriz de marca de propriedade dimensionada.</span><span class="sxs-lookup"><span data-stu-id="8e579-129">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the memory for the entry identifier of the PAB and the sized property tag array.</span></span> 
    

