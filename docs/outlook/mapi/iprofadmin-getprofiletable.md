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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309545"
---
# <a name="iprofadmingetprofiletable"></a><span data-ttu-id="8b16f-103">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="8b16f-103">IProfAdmin::GetProfileTable</span></span>

  
  
<span data-ttu-id="8b16f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b16f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b16f-105">Fornece acesso à tabela de perfil, uma tabela que contém informações sobre todos os perfis disponíveis.</span><span class="sxs-lookup"><span data-stu-id="8b16f-105">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="8b16f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8b16f-106">Parameters</span></span>

 <span data-ttu-id="8b16f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8b16f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8b16f-108">no Sempre nulo.</span><span class="sxs-lookup"><span data-stu-id="8b16f-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="8b16f-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="8b16f-109">_lppTable_</span></span>
  
> <span data-ttu-id="8b16f-110">bota Um ponteiro para um ponteiro para a tabela de perfis.</span><span class="sxs-lookup"><span data-stu-id="8b16f-110">[out] A pointer to a pointer to the profile table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8b16f-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8b16f-111">Return value</span></span>

<span data-ttu-id="8b16f-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="8b16f-112">S_OK</span></span> 
  
> <span data-ttu-id="8b16f-113">A tabela de perfil foi recuperada com êxito.</span><span class="sxs-lookup"><span data-stu-id="8b16f-113">The profile table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8b16f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b16f-114">Remarks</span></span>

<span data-ttu-id="8b16f-115">O método **IProfAdmin::** getprofiletable fornece acesso à tabela de perfis, que contém uma linha para cada perfil disponível.</span><span class="sxs-lookup"><span data-stu-id="8b16f-115">The **IProfAdmin::GetProfileTable** method provides access to the profile table, which contains one row for every available profile.</span></span> <span data-ttu-id="8b16f-116">Há apenas duas colunas em cada linha: o nome de exibição do perfil e um sinalizador que indica se o perfil é o padrão.</span><span class="sxs-lookup"><span data-stu-id="8b16f-116">There are only two columns in each row: the profile's display name, and a flag that indicates whether the profile is the default.</span></span> 
  
<span data-ttu-id="8b16f-117">Os perfis excluídos ou que estão em uso, mas que foram marcados para exclusão, não estão incluídos na tabela de perfis.</span><span class="sxs-lookup"><span data-stu-id="8b16f-117">Profiles that have been deleted, or that are in use but have been marked for deletion, are not included in the profile table.</span></span> <span data-ttu-id="8b16f-118">A tabela de perfil é estática; adições e exclusões subsequentes de perfis não são refletidas na tabela.</span><span class="sxs-lookup"><span data-stu-id="8b16f-118">The profile table is static; subsequent additions and deletions of profiles are not reflected in the table.</span></span> 
  
<span data-ttu-id="8b16f-119">Se não existir nenhum perfil \*\*\*\* , getprofiletable retornará uma tabela com zero linhas.</span><span class="sxs-lookup"><span data-stu-id="8b16f-119">If no profiles exist, **GetProfileTable** returns a table with zero rows.</span></span> 
  
<span data-ttu-id="8b16f-120">Para obter mais informações sobre a tabela de perfil, consulte [tabelas de perfil](profile-tables.md).</span><span class="sxs-lookup"><span data-stu-id="8b16f-120">For more information about the profile table, see [Profile Tables](profile-tables.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8b16f-121">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="8b16f-121">MFCMAPI reference</span></span>

<span data-ttu-id="8b16f-122">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8b16f-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8b16f-123">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="8b16f-123">**File**</span></span>|<span data-ttu-id="8b16f-124">**Função**</span><span class="sxs-lookup"><span data-stu-id="8b16f-124">**Function**</span></span>|<span data-ttu-id="8b16f-125">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="8b16f-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8b16f-126">MainDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="8b16f-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="8b16f-127">CMainDlg:: OnShowProfiles</span><span class="sxs-lookup"><span data-stu-id="8b16f-127">CMainDlg::OnShowProfiles</span></span>  <br/> |<span data-ttu-id="8b16f-128">MFCMAPI usa o método **IProfAdmin::** getprofiletable para fazer com que a tabela de perfil seja exibida em uma nova caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8b16f-128">MFCMAPI uses the **IProfAdmin::GetProfileTable** method to get the profile table to display in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8b16f-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b16f-129">See also</span></span>



[<span data-ttu-id="8b16f-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8b16f-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="8b16f-131">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="8b16f-131">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="8b16f-132">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8b16f-132">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="8b16f-133">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="8b16f-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

