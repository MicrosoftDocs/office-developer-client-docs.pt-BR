---
title: Método STAT - ActiveX Data Objects (ADO)
TOCTitle: Stat method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 853d89bde9184bd546b3e7df9e8eda287faf86c9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721070"
---
# <a name="stat-method-ado"></a>Método Stat (ADO)

**Aplica-se a**: Access 2013, o Office 2013

Recupera informações sobre um objeto **Stream**.

## <a name="syntax"></a>Sintaxe

Long *stream*. Stat (*StatStg*, *StatFlag*)

## <a name="return-value"></a>Valor de retorno

Um valor long que indica o status da operação.

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*StatStg* |Uma estrutura STATSTG que será preenchida com informações sobre o fluxo. A implementação do método Stat utilizada pelo objeto Stream do ADO não preenche todos os campos da estrutura.|
|*StatFlag* |Especifica que este método não retorna alguns dos membros na estrutura STATSTG, economizando dessa forma uma operação de alocação de memória. Os valores são obtidos da enumeração STATFLAG.<br/><br/>A enumeração STATFLAG tem dois valores:<br/>-STATFLAG_DEFAULT: 0<br/>-STATFLAG_NONAME: 1 |


## <a name="remarks"></a>Comentários

A versão do método Stat implementada para o objeto Stream do ADO preenche os seguintes campos da estrutura STATSTG:

|Campo|Descrição|
|:--------|:----------|
|*pwcsName* |Valor de uma cadeia de caracteres contendo o nome do fluxo, caso alguma esteja disponível e o StatFlag STATFLAG\_sem nome não foi especificado.|
|*cbSize* |Especifica o tamanho em bytes do fluxo ou matriz de bytes.|
|*mtime* |Indica a hora da última modificação para esse repositório, fluxo ou matriz de bytes.|
|*ctime* |Indica a hora da criação para esse repositório, fluxo ou matriz de bytes.|
|*atime* |Indica a hora do último acesso para esse repositório, fluxo ou matriz de bytes.|

Se STATFLAG\_sem nome for especificado no parâmetro StatFlag, o nome do fluxo não será retornado.

Se STATFLAG\_sem nome não foi especificado no parâmetro StatFlag e não há nenhum nome disponível para o fluxo atual, esse valor será f\_NOTIMPL.

