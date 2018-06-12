---
title: Definir a ordem de resolução de listas de endereços de forma programática
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f9559afb-8db1-ce72-3e11-9b3d47bb80b6
description: 'Modificado pela última vez: 06 de julho de 2012'
ms.openlocfilehash: 676d74c6441716203006f2db3e4a7d5777320a98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766738"
---
# <a name="programmatically-set-the-resolution-order-for-address-lists"></a><span data-ttu-id="d5532-103">Definir a ordem de resolução de listas de endereços de forma programática</span><span class="sxs-lookup"><span data-stu-id="d5532-103">Programmatically set the resolution order for address lists</span></span>
  
<span data-ttu-id="d5532-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d5532-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d5532-105">Este tópico contém um exemplo de código em C++ que programaticamente define a ordem das listas de endereços pelos quais destinatários em email participantes em solicitações de reunião e mensagens forem resolvidos.</span><span class="sxs-lookup"><span data-stu-id="d5532-105">This topic contains a code sample in C++ that programmatically sets the order of address lists by which recipients in email messages and attendees in meeting requests are resolved.</span></span>
  
<span data-ttu-id="d5532-106">Na MAPI, cada perfil pode oferecer suporte a várias listas de endereços e cada lista de endereços reside no seu próprio contêiner.</span><span class="sxs-lookup"><span data-stu-id="d5532-106">In MAPI, each profile can support multiple address lists and each address list resides in its own container.</span></span> <span data-ttu-id="d5532-107">MAPI oferece suporte ao método **[SetSearchPath](http://support.microsoft.com/kb/292590)** na interface do que permite que você defina um novo caminho de pesquisa no perfil que será usado para resolução de nome.</span><span class="sxs-lookup"><span data-stu-id="d5532-107">MAPI supports the **[SetSearchPath](http://support.microsoft.com/kb/292590)** method in the interface that allows you to set a new search path in the profile that is used for name resolution.</span></span> <span data-ttu-id="d5532-108">Para usar o método **IAddrBook::SetSearchPath** , você precisará definir a ordem de resolução desejada em uma matriz de **[SRowSet](srowset.md)** que mantém os contêineres dos catálogos de endereços relevantes na ordem desejada e, em seguida, especifique a matriz como a *lpSearchPath*  Use o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d5532-108">To use the **IAddrBook::SetSearchPath** method, you have to define the desired resolution order in a **[SRowSet](srowset.md)** array that holds the containers of the relevant address books in the desired order, and then specify the array as the  *lpSearchPath*  parameter.</span></span> <span data-ttu-id="d5532-109">A primeira propriedade para cada entrada na matriz **SRowSet** deve ser a propriedade **[PR_ENTRYID](pidtagentryid-canonical-property.md)** do catálogo de endereços correspondente.</span><span class="sxs-lookup"><span data-stu-id="d5532-109">The first property for each entry in the **SRowSet** array must be the **[PR_ENTRYID](pidtagentryid-canonical-property.md)** property of the corresponding address book.</span></span> 
  
<span data-ttu-id="d5532-110">O exemplo de código define a ordem de resolução nas etapas a seguir:</span><span class="sxs-lookup"><span data-stu-id="d5532-110">The code sample sets the resolution order in the following steps:</span></span>
  
1. <span data-ttu-id="d5532-111">Inicializa `numANR` ao número de contêineres para corresponder e especifica os nomes e a ordem de resolução das listas de endereço desejado em um `ANROrder` matriz.</span><span class="sxs-lookup"><span data-stu-id="d5532-111">Initializes  `numANR` to the number of containers to match, and specifies the names and resolution order of the desired address lists in an  `ANROrder` array.</span></span> 
    
2. <span data-ttu-id="d5532-112">Inicializa MAPI usando a função **MAPIInitialize** .</span><span class="sxs-lookup"><span data-stu-id="d5532-112">Initializes MAPI by using the **MAPIInitialize** function.</span></span> 
    
3.  <span data-ttu-id="d5532-113">Faça logon em MAPI e permite ao usuário escolher um perfil.</span><span class="sxs-lookup"><span data-stu-id="d5532-113">Logs on to MAPI and allows the user to choose a profile.</span></span> 
    
4.  <span data-ttu-id="d5532-114">Obtém um ponteiro para o catálogo de endereços da sessão atual.</span><span class="sxs-lookup"><span data-stu-id="d5532-114">Gets a pointer to the address book from the current session.</span></span> 
    
5. <span data-ttu-id="d5532-115">Abre o catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="d5532-115">Opens the Address Book.</span></span>
    
6. <span data-ttu-id="d5532-116">Abre o contêiner para a raiz do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="d5532-116">Opens the container for the root Address Book.</span></span>
    
7. <span data-ttu-id="d5532-117">Abre a tabela de hierarquia do contêiner de catálogo de endereços raiz.</span><span class="sxs-lookup"><span data-stu-id="d5532-117">Opens the hierarchy table of the root address book container.</span></span>
    
8. <span data-ttu-id="d5532-118">Obtém a lista de endereço contêineres do catálogo na hierarquia.</span><span class="sxs-lookup"><span data-stu-id="d5532-118">Gets the list of address book containers in the hierarchy.</span></span>
    
9. <span data-ttu-id="d5532-119">Procura as identificações de entrada das listas de endereços desejado, comparando os nomes das listas de endereço desejado no `ANROrder` aos nomes existentes na hierarquia de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="d5532-119">Looks for the entry IDs of the desired address lists by comparing the names of the desired address lists in  `ANROrder` to the existing names in the address book hierarchy.</span></span> 
    
10. <span data-ttu-id="d5532-120">Define as IDs da entrada apropriado à matriz **SRowSet** `pNewRows`.</span><span class="sxs-lookup"><span data-stu-id="d5532-120">Sets the appropriate entry IDs to the **SRowSet** array,  `pNewRows`.</span></span>
    
11. <span data-ttu-id="d5532-121">Chamará e passará `pNewRows` como o parâmetro *lpSearchPath* para **IAddrBook::SetSearchPath** para definir o caminho de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d5532-121">Calls and passes  `pNewRows` as the  *lpSearchPath*  parameter to **IAddrBook::SetSearchPath** to set the search path.</span></span> 
    
12. <span data-ttu-id="d5532-122">Limpa os ponteiros e buffers internos.</span><span class="sxs-lookup"><span data-stu-id="d5532-122">Cleans up internal buffers and pointers.</span></span>
    
13. <span data-ttu-id="d5532-123">Efetua logoff de MAPI.</span><span class="sxs-lookup"><span data-stu-id="d5532-123">Logs off from MAPI.</span></span>
    
14. <span data-ttu-id="d5532-124">Uninitalizes MAPI.</span><span class="sxs-lookup"><span data-stu-id="d5532-124">Uninitalizes MAPI.</span></span>
    
<span data-ttu-id="d5532-125">Este exemplo de código usa listas de endereços que estão disponíveis na instalação padrão do Microsoft Office Outlook: **Todos os contatos**, **Todos os grupos**e **Contatos**.</span><span class="sxs-lookup"><span data-stu-id="d5532-125">This code sample uses address lists that are available in the default installation of Microsoft Office Outlook: **All Contacts**, **All Groups**, and **Contacts**.</span></span> <span data-ttu-id="d5532-126">Você deve executar a amostra depois que o Outlook é iniciado e está sendo executado em um perfil inicializado.</span><span class="sxs-lookup"><span data-stu-id="d5532-126">You must run the sample after Outlook is started and is running on an initialized profile.</span></span> <span data-ttu-id="d5532-127">O exemplo funciona bem com nomes que estão em um idioma (por exemplo, todos os nomes são em inglês).</span><span class="sxs-lookup"><span data-stu-id="d5532-127">The sample works well with names that are in one language (for example, all names are in English).</span></span> <span data-ttu-id="d5532-128">Ele não é projetado para funcionar em implantações multilíngue, por exemplo, a pasta **Contatos** localizada para um usuário executando um build não são em inglês do Outlook.</span><span class="sxs-lookup"><span data-stu-id="d5532-128">It is not designed to work in multi-lingual deployments, for example the **Contacts** folder localized for a user running a non-English Outlook build.</span></span> 
  
```cpp
#include "stdafx.h" 
#include <mapix.h> 
#include <mapiguid.h> 
#include <mapiutil.h> 
#include <mapidefs.h> 
#include <stdio.h> 
#include <conio.h> 
 
//Number of address lists to resolve against 
const int numANR = 3; 
WCHAR *ANROrder[numANR] = {_T("All Contacts"), _T("All Groups"), _T("Contacts")}; 
UINT  numContainersFound [numANR] = {0}; 
 
// Temporary structure to allocate buffer in MAPI. This will be used as a parent buffer to free space later. 
LPVOID tempLink; 
 
// Forward declaration of helper function to copy binary data 
STDMETHODIMP CopySBinary( 
    LPSBinary psbDest, 
    const LPSBinary psbSrc, 
    LPVOID pParent); 
 
void main() 
{ 
    // MAPI address book and session variables 
    HRESULT       hRes = S_OK;            // Result code returned from MAPI calls. 
    LPMAPISESSION lpSession = NULL;   // Pointer to MAPI session. 
    LPADRBOOK     lpAddrBook = NULL;  // Pointer to Address Book. 
 
    // Counters 
    ULONG         i = 0;                  // Index counter 
    ULONG         j = 0;                  // Index counter 
 
    // Used for querying hierarchy 
    ULONG                                   ulObjType = 0L;      // Object type returned by MAPI 
    LPMAPICONTAINER     pIABRoot = NULL;     // Root address book container 
    LPMAPITABLE              pHTable = NULL;      // Holds hierarchy table 
    LPSRowSet        pRows = NULL;        // Pointer to row set. Stores AB Address Lists 
 
    // Used for setting search path 
    LPSRowSet     pNewRows = NULL;        // Pointer to new row set 
    SizedSRowSet  (numANR, NewRows);      // New row set 
    SPropValue    sProps[numANR] = {0};   // Property tag structure 
 
    // Structures contaning MAPI Column Sets required for querying tables 
    enum { 
        abPR_ENTRYID, 
        abPR_DISPLAY_NAME_W, 
        abNUM_COLS}; 
 
    static SizedSPropTagArray(abNUM_COLS,abCols) = { 
        abNUM_COLS, 
        PR_ENTRYID, 
        PR_DISPLAY_NAME_W, 
    }; 
 
    // Initialize MAPI 
    if (FAILED ( hRes = MAPIInitialize(NULL))) goto Exit; 
 
    // Log on to MAPI and allow user to choose profile 
 
    // Note: This uses the current MAPI session if there is one 
    if (FAILED ( hRes = MAPILogonEx(NULL, NULL, NULL, MAPI_LOGON_UI, &lpSession))) goto Exit; 
 
    // Open the Address Book 
    if (FAILED (hRes = lpSession->OpenAddressBook(NULL, NULL, NULL, &lpAddrBook))) goto Cleanup; 
 
    // Open the Address Book Root container 
    if (FAILED (hRes = lpAddrBook -> OpenEntry ( 
        0L,  
        NULL, 
        NULL,  
        0L, 
        &ulObjType, 
        (LPUNKNOWN *) &pIABRoot ))) 
    goto Cleanup; 
 
    // Intentionally allocate 0 bytes. This is used for buffer management. 
    MAPIAllocateBuffer(0L, &tempLink);  
 
    // Make sure there is a Container object 
    // Query hierarchy for containers 
    if ( MAPI_ABCONT == ulObjType ) { 
        // - Call IMAPIContainer::GetHierarchyTable to open the Hierarchy 
        //   table of the root address book container 
        if ( FAILED ( hRes = pIABRoot -> GetHierarchyTable ( CONVENIENT_DEPTH | MAPI_UNICODE, 
            &pHTable ) ) ) 
        goto Cleanup; 
 
        // Get the list of address book containers first 
        if ( FAILED ( hRes = HrQueryAllRows (  
            pHTable, 
            (LPSPropTagArray) &abCols, 
            NULL, 
            NULL, 
            0L, 
            &pRows ) ) ) 
        goto Cleanup; 
 
        // Initialize the structures to set the search order 
        ZeroMemory(&NewRows, numANR * sizeof(SRow)); 
        pNewRows = (LPSRowSet)&NewRows; 
 
        // Set the number of rows you are going to set 
        pNewRows->cRows = numANR; 
 
        // Set the pointers to the structures 
        for (i=0; i<numANR; i++) 
            pNewRows->aRow[i].lpProps = &sProps[i]; 
 
        // Compare the list to the ones that of interest 
        for (i=0; i<pRows->cRows; i++) { 
            if (pRows->aRow[i].lpProps[abPR_DISPLAY_NAME_W].ulPropTag == PR_DISPLAY_NAME_W) { 
                LPWSTR containerName =  pRows->aRow[i].lpProps[abPR_DISPLAY_NAME_W].Value.lpszW; 
                for (j=0; j<numANR; j++) 
                    if (!wcscmp (containerName, ANROrder[j])) { 
                        // First check if a container with this name has been found already 
                        if (numContainersFound[j] == 0) { 
                            numContainersFound[j]++; 
                            pNewRows->aRow[j].cValues = 1; 
 
                            // The property being passing is PR_ENTRY_ID 
                            pNewRows->aRow[j].lpProps[0].ulPropTag = PR_ENTRYID; 
 
                            // Copy the binary data over 
                            if (FAILED (hRes = CopySBinary( 
                                &pNewRows->aRow[j].lpProps[0].Value.bin, 
                                &pRows->aRow[i].lpProps[abPR_ENTRYID].Value.bin, 
                                tempLink))) {  
                                    printf ("Fatal Error:Failed to copy entry IDs\n"); 
                                    goto Cleanup; 
                            } 
                         } 
                         // More than 1 container matched the same name 
                         else {  
                             printf ("Fatal Error: Duplicate container found, container name = %s\n", containerName); 
                             goto Cleanup; 
                         } 
                    } 
            } 
        } 
 
        // Only set the search path if all the rows have been found 
        // Check the array for any entries that were blank 
        for (i=0; i< numANR; i++) 
            if (numContainersFound [i] == 0) { 
                printf ("Fatal Error: all containers were not found\n"); 
                goto Cleanup; 
            } 
 
        // Everything is safe to set the search path now 
        if (FAILED (hRes = lpAddrBook->SetSearchPath(0, pNewRows))) {                    
            printf ("Fatal Error: failed to set the search path\n"); 
            goto Cleanup; 
        } 
    } 
 
    Cleanup: 
        MAPIFreeBuffer(tempLink); 
        UlRelease(pHTable); 
        FreeProws(pRows); 
        UlRelease (pIABRoot); 
        UlRelease(lpAddrBook); 
 
        // Log off from MAPI 
        hRes = lpSession->Logoff(NULL, NULL, 0); 
        UlRelease(lpSession); 
 
    Exit: 
        // Uninitialize MAPI 
        MAPIUninitialize(); 
} 
 
///////////////////////////////////////////////////////////// 
//    CopySBinary() 
// 
//    Parameters 
// 
//    Purpose 
//      Allocates a new SBinary and copies psbSrc into it 
// 
 
STDMETHODIMP CopySBinary( 
    LPSBinary psbDest, 
    const LPSBinary psbSrc, 
    LPVOID pParent) 
{ 
    HRESULT     hRes = S_OK; 
    psbDest->cb = psbSrc->cb; 
 
    if (psbSrc->cb) { 
        if (pParent) 
            hRes = MAPIAllocateMore( 
                 psbSrc->cb, 
                 pParent, 
                 (LPVOID*) &psbDest->lpb); 
        else 
            hRes = MAPIAllocateBuffer( 
                 psbSrc->cb, 
                 (LPVOID*) &psbDest->lpb); 
 
    if (!FAILED(hRes)) 
        CopyMemory(psbDest->lpb,psbSrc->lpb,psbSrc->cb); 
    } 
 
   return hRes; 
} 

```

## <a name="see-also"></a><span data-ttu-id="d5532-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5532-129">See also</span></span>

- [<span data-ttu-id="d5532-130">Sobre como definir a ordem de resolução de listas de endereços no Outlook</span><span class="sxs-lookup"><span data-stu-id="d5532-130">About Setting the Resolution Order for Address Lists in Outlook</span></span>](about-setting-the-resolution-order-for-address-lists-in-outlook.md)

