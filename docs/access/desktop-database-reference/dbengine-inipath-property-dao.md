---
title: DBEngine.IniPath (DAO)
TOCTitle: IniPath Property
ms:assetid: b18cace5-4e53-d011-6373-f4ac64556fd4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822009(v=office.15)
ms:contentKeyID: 48547151
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053070
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f14f9f2d028bb8a9a8e71bc9d7b97ea5672466f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294292"
---
# <a name="dbengineinipath-property-dao"></a><span data-ttu-id="a7f4f-102">DBEngine.IniPath (DAO)</span><span class="sxs-lookup"><span data-stu-id="a7f4f-102">DBEngine.IniPath property (DAO)</span></span>


<span data-ttu-id="a7f4f-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a7f4f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a7f4f-104">Define ou retorna informações sobre a chave do Registro do Windows que contém os valores do mecanismo do banco de dados do Microsoft Access (somente em espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="a7f4f-104">Sets or returns information about the Windows Registry key that contains values for the Microsoft Access database engine (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="a7f4f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7f4f-105">Syntax</span></span>

<span data-ttu-id="a7f4f-106">*expressão* . IniPath</span><span class="sxs-lookup"><span data-stu-id="a7f4f-106">*expression* .IniPath</span></span>

<span data-ttu-id="a7f4f-107">*expressão* Uma variável que representa um objeto **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7f4f-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7f4f-108">Remarks</span></span>

<span data-ttu-id="a7f4f-109">Você pode configurar o mecanismo de banco de dados do Microsoft Access com o Registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-109">You can configure the Microsoft Access database engine with the Windows Registry.</span></span> <span data-ttu-id="a7f4f-110">Use o Registro para definir as opções, como DLLs instaláveis do ISAM.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-110">You can use the Registry to set options, such as installable ISAM DLLs.</span></span>

<span data-ttu-id="a7f4f-p102">Para essa opção ter efeito, defina a propriedade **IniPath** antes de o aplicativo chamar qualquer outro código do DAO. O escopo dessa configuração está limitado ao aplicativo e não pode ser alterado sem reiniciar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-p102">For this option to have any effect, you must set the **IniPath** property before your application invokes any other DAO code. The scope of this setting is limited to your application and can't be changed without restarting your application.</span></span>

<span data-ttu-id="a7f4f-p103">Também é possível usar o Registro para fornecer os parâmetros de inicialização de alguns drivers dos bancos de dados ISAM instaláveis. Por exemplo, para usar o Paradox versão 4.0, defina a propriedade **IniPath** como uma parte do Registro que contém os parâmetros adequados.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-p103">You also use the Registry to provide initialization parameters for some installable ISAM database drivers. For example, to use Paradox version 4.0, set the **IniPath** property to a part of the Registry containing the appropriate parameters.</span></span>

<span data-ttu-id="a7f4f-115">Essa propriedade reconhece A MÁQUINA LOCAL HKEY \_ ou O USUÁRIO LOCAL \_ \_ HKEY. \_</span><span class="sxs-lookup"><span data-stu-id="a7f4f-115">This property recognizes either HKEY\_LOCAL\_MACHINE or HKEY\_LOCAL\_USER.</span></span> <span data-ttu-id="a7f4f-116">Se nenhuma chave raiz for fornecida, o padrão é HKEY \_ LOCAL \_ MACHINE.</span><span class="sxs-lookup"><span data-stu-id="a7f4f-116">If no root key is supplied, the default is HKEY\_LOCAL\_MACHINE.</span></span>

