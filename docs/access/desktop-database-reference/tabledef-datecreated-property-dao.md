---
title: Propriedade TableDef.DateCreated (DAO)
TOCTitle: DateCreated Property
ms:assetid: fedd28e9-41a4-db7f-9ba9-6ada350d594a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837292(v=office.15)
ms:contentKeyID: 48548947
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be76ed7f9d358963ea58776327ddafbb66f9d367
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923137"
---
# <a name="tabledefdatecreated-property-dao"></a><span data-ttu-id="df1fc-102">Propriedade TableDef.DateCreated (DAO)</span><span class="sxs-lookup"><span data-stu-id="df1fc-102">TableDef.DateCreated property (DAO)</span></span>


<span data-ttu-id="df1fc-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="df1fc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="df1fc-p101">Retorna a hora e a data nas quais um objeto foi criado (somente em espaços de trabalho do Microsoft Access). **Variant** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="df1fc-p101">Returns the date and time that an object was created (Microsoft Access workspaces only). Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="df1fc-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df1fc-106">Syntax</span></span>

<span data-ttu-id="df1fc-107">*expressão* . DateCreated</span><span class="sxs-lookup"><span data-stu-id="df1fc-107">*expression* .DateCreated</span></span>

<span data-ttu-id="df1fc-108">*expressão* Uma variável que representa um objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="df1fc-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="df1fc-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="df1fc-109">Remarks</span></span>

<span data-ttu-id="df1fc-p102">**DateCreated** e **LastUpdated** retornam a data e a hora em que o objeto foi criado ou atualizado pela última vez. Em um ambiente de vários usuários, os usuários devem obter essas configurações diretamente do servidor de arquivos para evitar discrepâncias nas configurações das propriedades DateCreated e LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="df1fc-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

