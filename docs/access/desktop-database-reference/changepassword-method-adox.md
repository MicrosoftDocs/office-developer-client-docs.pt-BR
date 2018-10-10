---
title: Método ChangePassword (ADOX)
TOCTitle: ChangePassword Method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2bd2f5d87c6f90e940858ce5c6e01099c5e539d4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462302"
---
# <a name="changepassword-method-adox"></a><span data-ttu-id="97fe7-102">Método ChangePassword (ADOX)</span><span class="sxs-lookup"><span data-stu-id="97fe7-102">ChangePassword Method (ADOX)</span></span>


<span data-ttu-id="97fe7-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="97fe7-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="97fe7-104">Altera a senha de uma conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="97fe7-104">Changes the password for a user account.</span></span>

## <a name="syntax"></a><span data-ttu-id="97fe7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="97fe7-105">Syntax</span></span>

<span data-ttu-id="97fe7-106">O *usuário*. ChangePassword*senhaantiga*, *NewPassword*</span><span class="sxs-lookup"><span data-stu-id="97fe7-106">*User*.ChangePassword*OldPassword*, *NewPassword*</span></span>

## <a name="parameters"></a><span data-ttu-id="97fe7-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97fe7-107">Parameters</span></span>

  - <span data-ttu-id="97fe7-108">*Senhaantiga*</span><span class="sxs-lookup"><span data-stu-id="97fe7-108">*OldPassword*</span></span>

  - <span data-ttu-id="97fe7-p101">Um valor **String** que especifica a senha existente do usuário. Se o usuário não tiver uma senha no momento, usar uma sequência vazia ("") para *OldPassword*.</span><span class="sxs-lookup"><span data-stu-id="97fe7-p101">A **String** value that specifies the user's existing password. If the user doesn't currently have a password, use an empty string ("") for *OldPassword*.</span></span>

  - <span data-ttu-id="97fe7-111">*NewPassword*</span><span class="sxs-lookup"><span data-stu-id="97fe7-111">*NewPassword*</span></span>

  - <span data-ttu-id="97fe7-112">Um valor **String** que especifica a nova senha.</span><span class="sxs-lookup"><span data-stu-id="97fe7-112">A **String** value that specifies the new password.</span></span>

## <a name="remarks"></a><span data-ttu-id="97fe7-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="97fe7-113">Remarks</span></span>

<span data-ttu-id="97fe7-114">Por motivos de segurança, a senha antiga deve ser especificada, além da nova senha.</span><span class="sxs-lookup"><span data-stu-id="97fe7-114">For security reasons, the old password must be specified in addition to the new password.</span></span>

<span data-ttu-id="97fe7-115">Ocorrerá um erro se o provedor não oferecer suporte para a administração de propriedades de objetos de confiança.</span><span class="sxs-lookup"><span data-stu-id="97fe7-115">An error will occur if the provider does not support the administration of trustee properties.</span></span>

