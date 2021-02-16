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
ms.openlocfilehash: 2db7dba67e7b71df6921ecd97189255a0ef7823a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414640"
---
# <a name="iprofadmingetprofiletable"></a><span data-ttu-id="1f352-103">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="1f352-103">IProfAdmin::GetProfileTable</span></span>

  
  
<span data-ttu-id="1f352-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f352-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f352-105">Fornece acesso à tabela de perfil, uma tabela que contém informações sobre todos os perfis disponíveis.</span><span class="sxs-lookup"><span data-stu-id="1f352-105">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="1f352-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f352-106">Parameters</span></span>

 <span data-ttu-id="1f352-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1f352-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1f352-108">[in] Sempre NULO.</span><span class="sxs-lookup"><span data-stu-id="1f352-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="1f352-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="1f352-109">_lppTable_</span></span>
  
> <span data-ttu-id="1f352-110">[out] Um ponteiro para um ponteiro para a tabela de perfil.</span><span class="sxs-lookup"><span data-stu-id="1f352-110">[out] A pointer to a pointer to the profile table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1f352-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1f352-111">Return value</span></span>

<span data-ttu-id="1f352-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="1f352-112">S_OK</span></span> 
  
> <span data-ttu-id="1f352-113">A tabela de perfil foi recuperada com êxito.</span><span class="sxs-lookup"><span data-stu-id="1f352-113">The profile table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1f352-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f352-114">Remarks</span></span>

<span data-ttu-id="1f352-115">O **método IProfAdmin::GetProfileTable** fornece acesso à tabela de perfil, que contém uma linha para cada perfil disponível.</span><span class="sxs-lookup"><span data-stu-id="1f352-115">The **IProfAdmin::GetProfileTable** method provides access to the profile table, which contains one row for every available profile.</span></span> <span data-ttu-id="1f352-116">Há apenas duas colunas em cada linha: o nome de exibição do perfil e um sinalizador que indica se o perfil é o padrão.</span><span class="sxs-lookup"><span data-stu-id="1f352-116">There are only two columns in each row: the profile's display name, and a flag that indicates whether the profile is the default.</span></span> 
  
<span data-ttu-id="1f352-117">Perfis que foram excluídos ou que estão em uso, mas foram marcados para exclusão, não estão incluídos na tabela de perfil.</span><span class="sxs-lookup"><span data-stu-id="1f352-117">Profiles that have been deleted, or that are in use but have been marked for deletion, are not included in the profile table.</span></span> <span data-ttu-id="1f352-118">A tabela de perfil é estática; adições e exclusões subsequentes de perfis não são refletidas na tabela.</span><span class="sxs-lookup"><span data-stu-id="1f352-118">The profile table is static; subsequent additions and deletions of profiles are not reflected in the table.</span></span> 
  
<span data-ttu-id="1f352-119">Se não existirem perfis, **GetProfileTable** retornará uma tabela com zero linhas.</span><span class="sxs-lookup"><span data-stu-id="1f352-119">If no profiles exist, **GetProfileTable** returns a table with zero rows.</span></span> 
  
<span data-ttu-id="1f352-120">Para obter mais informações sobre a tabela de perfil, consulte [Profile Tables](profile-tables.md).</span><span class="sxs-lookup"><span data-stu-id="1f352-120">For more information about the profile table, see [Profile Tables](profile-tables.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1f352-121">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1f352-121">MFCMAPI reference</span></span>

<span data-ttu-id="1f352-122">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1f352-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1f352-123">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="1f352-123">**File**</span></span>|<span data-ttu-id="1f352-124">**Função**</span><span class="sxs-lookup"><span data-stu-id="1f352-124">**Function**</span></span>|<span data-ttu-id="1f352-125">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="1f352-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1f352-126">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="1f352-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="1f352-127">CMainDlg::OnShowProfiles</span><span class="sxs-lookup"><span data-stu-id="1f352-127">CMainDlg::OnShowProfiles</span></span>  <br/> |<span data-ttu-id="1f352-128">MFCMAPI usa o **método IProfAdmin::GetProfileTable** para fazer com que a tabela de perfil seja exibida em uma nova caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1f352-128">MFCMAPI uses the **IProfAdmin::GetProfileTable** method to get the profile table to display in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1f352-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f352-129">See also</span></span>



[<span data-ttu-id="1f352-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1f352-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="1f352-131">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="1f352-131">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="1f352-132">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1f352-132">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="1f352-133">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="1f352-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

