---
title: Propriedade Handler (RDS)
TOCTitle: Handler Property (RDS)
ms:assetid: aaf8c8c6-f95b-3cf3-b3f6-203f37464c87
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249792(v=office.15)
ms:contentKeyID: 48546962
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dcb0b7f635e9ad74e6d8733a2f0fbe0153ac4739
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884867"
---
# <a name="handler-property-rds"></a><span data-ttu-id="eeba5-102">Propriedade Handler (RDS)</span><span class="sxs-lookup"><span data-stu-id="eeba5-102">Handler Property (RDS)</span></span>


<span data-ttu-id="eeba5-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="eeba5-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="eeba5-104">Indica o nome de um programa de personalização do servidor (manipulador) que estende a funcionalidade do [RDSServer.DataFactory](datafactory-object-rdsserver.md) e qualquer parâmetro usado pelo *manipulador*.</span><span class="sxs-lookup"><span data-stu-id="eeba5-104">Indicates the name of a server-side customization program (handler) that extends the functionality of the [RDSServer.DataFactory](datafactory-object-rdsserver.md), and any parameters used by the *handler*.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeba5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eeba5-105">Syntax</span></span>

<span data-ttu-id="eeba5-106">*DataControl*. Manipulador = *cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="eeba5-106">*DataControl*.Handler = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="eeba5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eeba5-107">Parameters</span></span>

  - <span data-ttu-id="eeba5-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="eeba5-108">*DataControl*</span></span>

  - <span data-ttu-id="eeba5-109">Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="eeba5-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="eeba5-110">*String*</span><span class="sxs-lookup"><span data-stu-id="eeba5-110">*String*</span></span>

  - <span data-ttu-id="eeba5-111">Um valor **String** que contém o nome do manipulador e qualquer parâmetro, todos separado por vírgulas (por exemplo, "handlerName, parm1, parm2,..., parm *N"*).</span><span class="sxs-lookup"><span data-stu-id="eeba5-111">A **String** value that contains the name of the handler and any parameters, all separated by commas (for example, "handlerName,parm1,parm2,...,parm *N*" ).</span></span>

## <a name="remarks"></a><span data-ttu-id="eeba5-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="eeba5-112">Remarks</span></span>

<span data-ttu-id="eeba5-113">Esta propriedade oferece suporte à personalização, uma funcionalidade que requer a definição da propriedade [CursorLocation](cursorlocation-property-ado.md) como **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="eeba5-113">This property supports customization, a functionality that requires setting the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**.</span></span>

<span data-ttu-id="eeba5-p101">O nome do manipulador e seus parâmetros, se houver, são separados por vírgulas (","). Um comportamento imprevisível ocorrerá se um ponto-e-vírgula (";") aparecer em qualquer lugar dentro do *String*. Você pode compor seu próprio manipulador, desde que ele ofereça suporte à interface **IDataFactoryHandler**.</span><span class="sxs-lookup"><span data-stu-id="eeba5-p101">The name of the handler and its parameters, if any, are separated by commas (","). Unpredictable behavior will result if a semicolon (";") appears anywhere within *String*. You can write your own handler, provided it supports the **IDataFactoryHandler** interface.</span></span>

<span data-ttu-id="eeba5-p102">O nome do manipulador padrão é **MSDFMAP.Handler** e seu parâmetro padrão é um arquivo de personalização chamado **MSDFMAP.INI**. Use esta propriedade para invocar arquivos de personalização alternativos pelo administrador do servidor.</span><span class="sxs-lookup"><span data-stu-id="eeba5-p102">The name of the default handler is **MSDFMAP.Handler**, and its default parameter is a customization file named **MSDFMAP.INI**. Use this property to invoke alternate customization files created by your server administrator.</span></span>

<span data-ttu-id="eeba5-119">A alternativa para definir a propriedade **Handler** é especificar um manipulador e os parâmetros na propriedade [ConnectionString](connectionstring-property-ado.md) ; ou seja, "\**manipulador = \* \* \* handlerName, parm1, parm2,...;*".</span><span class="sxs-lookup"><span data-stu-id="eeba5-119">The alternative to setting the **Handler** property is to specify a handler and parameters in the [ConnectionString](connectionstring-property-ado.md) property; that is, "\**Handler=\*\*\*handlerName,parm1,parm2,...;*".</span></span>

