---
title: Propriedade Handler (RDS)
TOCTitle: Handler property (RDS)
ms:assetid: aaf8c8c6-f95b-3cf3-b3f6-203f37464c87
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249792(v=office.15)
ms:contentKeyID: 48546962
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c3ad91f0a288b9908a5af5f92d7bfca3b23cdfe9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292066"
---
# <a name="handler-property-rds"></a><span data-ttu-id="5603a-102">Propriedade Handler (RDS)</span><span class="sxs-lookup"><span data-stu-id="5603a-102">Handler property (RDS)</span></span>

<span data-ttu-id="5603a-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5603a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5603a-104">Indica o nome de um programa de personalização do servidor (manipulador) que estende a funcionalidade do [RDSServer.DataFactory](datafactory-object-rdsserver.md) e qualquer parâmetro usado pelo *manipulador*.</span><span class="sxs-lookup"><span data-stu-id="5603a-104">Indicates the name of a server-side customization program (handler) that extends the functionality of the [RDSServer.DataFactory](datafactory-object-rdsserver.md), and any parameters used by the *handler*.</span></span>

## <a name="syntax"></a><span data-ttu-id="5603a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5603a-105">Syntax</span></span>

<span data-ttu-id="5603a-106">*DataControl*. Handler = *cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="5603a-106">*DataControl*.Handler = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="5603a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5603a-107">Parameters</span></span>

|<span data-ttu-id="5603a-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5603a-108">Parameter</span></span>|<span data-ttu-id="5603a-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="5603a-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="5603a-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="5603a-110">*DataControl*</span></span> |<span data-ttu-id="5603a-111">Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="5603a-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="5603a-112">*String*</span><span class="sxs-lookup"><span data-stu-id="5603a-112">*String*</span></span> |<span data-ttu-id="5603a-113">Um valor **String** que contém o nome do manipulador e qualquer parâmetro, todos separados por vírgulas (por exemplo, "HandlerName, Parm1, parm2,..., Parm *N*").</span><span class="sxs-lookup"><span data-stu-id="5603a-113">A **String** value that contains the name of the handler and any parameters, all separated by commas (for example, "handlerName,parm1,parm2,...,parm *N*" ).</span></span>|

## <a name="remarks"></a><span data-ttu-id="5603a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5603a-114">Remarks</span></span>

<span data-ttu-id="5603a-115">Esta propriedade oferece suporte à personalização, uma funcionalidade que requer a definição da propriedade [CursorLocation](cursorlocation-property-ado.md) como **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="5603a-115">This property supports customization, a functionality that requires setting the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**.</span></span>

<span data-ttu-id="5603a-p101">O nome do manipulador e seus parâmetros, se houver, são separados por vírgulas (","). Um comportamento imprevisível ocorrerá se um ponto-e-vírgula (";") aparecer em qualquer lugar dentro do *String*. Você pode compor seu próprio manipulador, desde que ele ofereça suporte à interface **IDataFactoryHandler**.</span><span class="sxs-lookup"><span data-stu-id="5603a-p101">The name of the handler and its parameters, if any, are separated by commas (","). Unpredictable behavior will result if a semicolon (";") appears anywhere within *String*. You can write your own handler, provided it supports the **IDataFactoryHandler** interface.</span></span>

<span data-ttu-id="5603a-p102">O nome do manipulador padrão é **MSDFMAP.Handler** e seu parâmetro padrão é um arquivo de personalização chamado **MSDFMAP.INI**. Use esta propriedade para invocar arquivos de personalização alternativos pelo administrador do servidor.</span><span class="sxs-lookup"><span data-stu-id="5603a-p102">The name of the default handler is **MSDFMAP.Handler**, and its default parameter is a customization file named **MSDFMAP.INI**. Use this property to invoke alternate customization files created by your server administrator.</span></span>

<span data-ttu-id="5603a-121">A alternativa para definir a propriedade **Handler** é especificar um manipulador e os parâmetros na propriedade [ConnectionString](connectionstring-property-ado.md) ; ou seja, "\**Handler = \* \* \* HandlerName, Parm1, parm2,...;*".</span><span class="sxs-lookup"><span data-stu-id="5603a-121">The alternative to setting the **Handler** property is to specify a handler and parameters in the [ConnectionString](connectionstring-property-ado.md) property; that is, "\**Handler=\*\*\*handlerName,parm1,parm2,...;*".</span></span>

