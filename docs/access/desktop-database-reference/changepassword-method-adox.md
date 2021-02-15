---
title: Método ChangePassword (ADOX)
TOCTitle: ChangePassword method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: df67774b9b38b5fbcc836a2ea0dfc17886d67107
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296525"
---
# <a name="changepassword-method-adox"></a><span data-ttu-id="4b954-102">Método ChangePassword (ADOX)</span><span class="sxs-lookup"><span data-stu-id="4b954-102">ChangePassword method (ADOX)</span></span>

<span data-ttu-id="4b954-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b954-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4b954-104">Altera a senha de uma conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="4b954-104">Changes the password for a user account.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b954-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b954-105">Syntax</span></span>

<span data-ttu-id="4b954-106">*Usuário*. ChangePassword *OldPassword*, *NewPassword*</span><span class="sxs-lookup"><span data-stu-id="4b954-106">*User*.ChangePassword *OldPassword*, *NewPassword*</span></span>

## <a name="parameters"></a><span data-ttu-id="4b954-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b954-107">Parameters</span></span>

|<span data-ttu-id="4b954-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="4b954-108">Parameter</span></span>|<span data-ttu-id="4b954-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b954-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="4b954-110">*OldPassword*</span><span class="sxs-lookup"><span data-stu-id="4b954-110">*OldPassword*</span></span> |<span data-ttu-id="4b954-111">Um valor **String** que especifica a senha existente do usuário.</span><span class="sxs-lookup"><span data-stu-id="4b954-111">A **String** value that specifies the user's existing password.</span></span> <span data-ttu-id="4b954-112">Se o usuário não tiver uma senha no momento, usar uma sequência vazia ("") para *OldPassword*.</span><span class="sxs-lookup"><span data-stu-id="4b954-112">If the user doesn't currently have a password, use an empty string ("") for *OldPassword*.</span></span>|
|<span data-ttu-id="4b954-113">*NewPassword*</span><span class="sxs-lookup"><span data-stu-id="4b954-113">*NewPassword*</span></span> |<span data-ttu-id="4b954-114">Um valor **String** que especifica a nova senha.</span><span class="sxs-lookup"><span data-stu-id="4b954-114">A **String** value that specifies the new password.</span></span>|

## <a name="remarks"></a><span data-ttu-id="4b954-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b954-115">Remarks</span></span>

<span data-ttu-id="4b954-116">Por motivos de segurança, a senha antiga deve ser especificada, além da nova senha.</span><span class="sxs-lookup"><span data-stu-id="4b954-116">For security reasons, the old password must be specified in addition to the new password.</span></span>

<span data-ttu-id="4b954-117">Ocorrerá um erro se o provedor não oferecer suporte para a administração de propriedades de objetos de confiança.</span><span class="sxs-lookup"><span data-stu-id="4b954-117">An error will occur if the provider does not support the administration of trustee properties.</span></span>

