---
title: Método ChangePassword (ADOX)
TOCTitle: ChangePassword method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e7e6d88b207fecc93b9a9bafa2d6b504456a3a3e
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949268"
---
# <a name="changepassword-method-adox"></a><span data-ttu-id="fb94c-102">Método ChangePassword (ADOX)</span><span class="sxs-lookup"><span data-stu-id="fb94c-102">ChangePassword method (ADOX)</span></span>

<span data-ttu-id="fb94c-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="fb94c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fb94c-104">Altera a senha de uma conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="fb94c-104">Changes the password for a user account.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb94c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb94c-105">Syntax</span></span>

<span data-ttu-id="fb94c-106">O *usuário*. ChangePassword*senhaantiga*, *NewPassword*</span><span class="sxs-lookup"><span data-stu-id="fb94c-106">*User*.ChangePassword*OldPassword*, *NewPassword*</span></span>

## <a name="parameters"></a><span data-ttu-id="fb94c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb94c-107">Parameters</span></span>

|<span data-ttu-id="fb94c-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb94c-108">Parameter</span></span>|<span data-ttu-id="fb94c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb94c-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="fb94c-110">*Senhaantiga*</span><span class="sxs-lookup"><span data-stu-id="fb94c-110">*OldPassword*</span></span> |<span data-ttu-id="fb94c-p101">Um valor **String** que especifica a senha existente do usuário. Se o usuário não tiver uma senha no momento, usar uma sequência vazia ("") para *OldPassword*.</span><span class="sxs-lookup"><span data-stu-id="fb94c-p101">A **String** value that specifies the user's existing password. If the user doesn't currently have a password, use an empty string ("") for *OldPassword*.</span></span>|
|<span data-ttu-id="fb94c-113">*NewPassword*</span><span class="sxs-lookup"><span data-stu-id="fb94c-113">*NewPassword*</span></span> |<span data-ttu-id="fb94c-114">Um valor **String** que especifica a nova senha.</span><span class="sxs-lookup"><span data-stu-id="fb94c-114">A **String** value that specifies the new password.</span></span>|

## <a name="remarks"></a><span data-ttu-id="fb94c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb94c-115">Remarks</span></span>

<span data-ttu-id="fb94c-116">Por motivos de segurança, a senha antiga deve ser especificada, além da nova senha.</span><span class="sxs-lookup"><span data-stu-id="fb94c-116">For security reasons, the old password must be specified in addition to the new password.</span></span>

<span data-ttu-id="fb94c-117">Ocorrerá um erro se o provedor não oferecer suporte para a administração de propriedades de objetos de confiança.</span><span class="sxs-lookup"><span data-stu-id="fb94c-117">An error will occur if the provider does not support the administration of trustee properties.</span></span>

