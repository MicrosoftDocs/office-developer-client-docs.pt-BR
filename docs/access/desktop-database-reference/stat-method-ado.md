---
title: Método STAT - ActiveX Data Objects (ADO)
TOCTitle: Stat Method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5d2b8c69df8caba93f693194573d057d52dffeb8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462426"
---
# <a name="stat-method-ado"></a>Método Stat (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Recupera informações sobre um objeto **Stream**.

## <a name="syntax"></a>Sintaxe

Long *stream*. Stat (*StatStg*, *StatFlag*)

## <a name="return-value"></a>Valor de Retorno

Um valor long que indica o status da operação.

## <a name="parameters"></a>Parâmetros

  - *StatStg*

  - Uma estrutura STATSTG que será preenchida com informações sobre o fluxo. A implementação do método Stat utilizada pelo objeto Stream do ADO não preenche todos os campos da estrutura.

  - *StatFlag*

  - Especifica que este método não retorna alguns dos membros na estrutura STATSTG, economizando dessa forma uma operação de alocação de memória. Os valores são obtidos da enumeração STATFLAG.  
      
    A enumeração STATFLAG tem dois valores
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p>Constant</p></th>
    <th><p>Value</p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p>STATFLAG_DEFAULT</p></td>
    <td><p>0</p></td>
    </tr>
    <tr class="even">
    <td><p>STATFLAG_NONAME</p></td>
    <td><p>1</p></td>
    </tr>
    </tbody>
    </table>


## <a name="remarks"></a>Comentários

A versão do método Stat implementada para o objeto Stream do ADO preenche os seguintes campos da estrutura STATSTG:

  - *pwcsName*

  - Valor de uma cadeia de caracteres contendo o nome do fluxo, caso alguma esteja disponível e o StatFlag STATFLAG\_sem nome não foi especificado.

  - *cbSize*

  - Especifica o tamanho em bytes do fluxo ou matriz de bytes.

  - *mtime*

  - Indica a hora da última modificação para esse repositório, fluxo ou matriz de bytes.

  - *ctime*

  - Indica a hora da criação para esse repositório, fluxo ou matriz de bytes.

  - *atime*

  - Indica a hora do último acesso para esse repositório, fluxo ou matriz de bytes.

Se STATFLAG\_sem nome for especificado no parâmetro StatFlag, o nome do fluxo não será retornado.

Se STATFLAG\_sem nome não foi especificado no parâmetro StatFlag e não há nenhum nome disponível para o fluxo atual, esse valor será f\_NOTIMPL.

