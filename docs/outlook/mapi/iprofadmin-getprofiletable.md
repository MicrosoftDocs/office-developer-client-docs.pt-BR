---
title: IProfAdminGetProfileTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetProfileTable
api_type:
- COM
ms.assetid: cebccd2d-8215-486e-9964-7fc42412cec6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8b1b037cf24c1bb5a0c84da3d59892ab15763f37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588241"
---
# <a name="iprofadmingetprofiletable"></a><span data-ttu-id="4c743-103">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="4c743-103">IProfAdmin::GetProfileTable</span></span>

  
  
<span data-ttu-id="4c743-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c743-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c743-105">Fornece acesso à tabela de perfis, uma tabela que contém informações sobre todos os perfis disponíveis.</span><span class="sxs-lookup"><span data-stu-id="4c743-105">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="4c743-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c743-106">Parameters</span></span>

 <span data-ttu-id="4c743-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4c743-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4c743-108">[in] Sempre nulo.</span><span class="sxs-lookup"><span data-stu-id="4c743-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="4c743-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="4c743-109">_lppTable_</span></span>
  
> <span data-ttu-id="4c743-110">[out] Um ponteiro para um ponteiro para a tabela de perfil.</span><span class="sxs-lookup"><span data-stu-id="4c743-110">[out] A pointer to a pointer to the profile table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4c743-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4c743-111">Return value</span></span>

<span data-ttu-id="4c743-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="4c743-112">S_OK</span></span> 
  
> <span data-ttu-id="4c743-113">A tabela de perfil foi recuperada com êxito.</span><span class="sxs-lookup"><span data-stu-id="4c743-113">The profile table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4c743-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c743-114">Remarks</span></span>

<span data-ttu-id="4c743-115">O método **IProfAdmin::GetProfileTable** fornece acesso à tabela de perfis, que contém uma linha para cada perfil disponível.</span><span class="sxs-lookup"><span data-stu-id="4c743-115">The **IProfAdmin::GetProfileTable** method provides access to the profile table, which contains one row for every available profile.</span></span> <span data-ttu-id="4c743-116">Existem apenas duas colunas em cada linha: nome para exibição do perfil e um sinalizador que indica se o perfil é o padrão.</span><span class="sxs-lookup"><span data-stu-id="4c743-116">There are only two columns in each row: the profile's display name, and a flag that indicates whether the profile is the default.</span></span> 
  
<span data-ttu-id="4c743-117">Perfis que tenha sido excluída, ou que estão em uso, mas foram marcadas para exclusão, não são incluídos na tabela de perfil.</span><span class="sxs-lookup"><span data-stu-id="4c743-117">Profiles that have been deleted, or that are in use but have been marked for deletion, are not included in the profile table.</span></span> <span data-ttu-id="4c743-118">A tabela de perfil é estática; subsequentes adições e exclusões de perfis não serão refletidas na tabela.</span><span class="sxs-lookup"><span data-stu-id="4c743-118">The profile table is static; subsequent additions and deletions of profiles are not reflected in the table.</span></span> 
  
<span data-ttu-id="4c743-119">Se nenhum perfil existir, **GetProfileTable** retorna uma tabela com zero linhas.</span><span class="sxs-lookup"><span data-stu-id="4c743-119">If no profiles exist, **GetProfileTable** returns a table with zero rows.</span></span> 
  
<span data-ttu-id="4c743-120">Para obter mais informações sobre a tabela de perfil, consulte [As tabelas de perfil](profile-tables.md).</span><span class="sxs-lookup"><span data-stu-id="4c743-120">For more information about the profile table, see [Profile Tables](profile-tables.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4c743-121">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4c743-121">MFCMAPI reference</span></span>

<span data-ttu-id="4c743-122">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4c743-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4c743-123">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="4c743-123">**File**</span></span>|<span data-ttu-id="4c743-124">**Function**</span><span class="sxs-lookup"><span data-stu-id="4c743-124">**Function**</span></span>|<span data-ttu-id="4c743-125">**Comment**</span><span class="sxs-lookup"><span data-stu-id="4c743-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4c743-126">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="4c743-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="4c743-127">CMainDlg::OnShowProfiles</span><span class="sxs-lookup"><span data-stu-id="4c743-127">CMainDlg::OnShowProfiles</span></span>  <br/> |<span data-ttu-id="4c743-128">MFCMAPI usa o método **IProfAdmin::GetProfileTable** para obter a tabela de perfil para exibir em uma nova caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4c743-128">MFCMAPI uses the **IProfAdmin::GetProfileTable** method to get the profile table to display in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4c743-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c743-129">See also</span></span>



[<span data-ttu-id="4c743-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4c743-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="4c743-131">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="4c743-131">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="4c743-132">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4c743-132">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="4c743-133">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="4c743-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

