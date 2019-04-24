---
title: Propriedade Recordset2. Filter (DAO)
TOCTitle: Filter Property
ms:assetid: 5b3b4e18-8af4-5acd-a129-513ba2d913d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194529(v=office.15)
ms:contentKeyID: 48545069
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053062
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 19f3c017aa5d4a353f3e832a3678d921565ea822
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307326"
---
# <a name="recordset2filter-property-dao"></a>Propriedade Recordset2. Filter (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Define ou retorna um valor que determina os registros incluídos em um objeto **Recordset** aberto posteriormente (somente nos espaços de trabalho do Microsoft Access). **String** de leitura/gravação.

## <a name="syntax"></a>Sintaxe

*expressão* . Filtre

*expressão* Uma expressão que retorna um objeto **Recordset2** .

## <a name="remarks"></a>Comentários

O valor de definição ou de retorno é um tipo de dados de cadeia de caracteres que contém a cláusula WHERE de uma instrução SQL sem a palavra reservada WHERE.

Use a propriedade **Filter** para aplicar um filtro a um objeto **Recordset** do tipo dynaset, instantâneo ou somente encaminhamento.

Você pode usar a propriedade **Filter** para restringir os registros retornados de um objeto existente quando um novo objeto **Recordset** for aberto com base em um objeto **Recordset** existente.

Use o formato de data dos EUA (mês-dia-ano) quando você filtrar campos que contenham datas, mesmo que não esteja usando a versão norte-americana do mecanismo de banco de dados do Microsoft Access (nesse caso, você deve montar qualquer data por meio da concatenação de cadeias de caracteres, por exemplo, strMonth & "-" _ aMP_ strDay & "-" & strYear). Caso contrário, é possível que os dados não sejam filtrados como esperado.

Em muitos casos, é mais rápido abrir um novo objeto **Recordset** pelo uso de uma instrução SQL que inclui a cláusula WHERE.

Se você definir a propriedade como uma cadeia de caracteres concatenada com um valor não inteiro e os parâmetros do sistema especificarem um caractere não norte-americano. decimal, como vírgula (por exemplo, strFilter = "PRICE \> " & lngPrice e lngPrice = 125, 50), ocorrerá um erro quando você tentar Abra o próximo **conjunto de registros**. Isso acontecerá porque durante a concatenação, o número será convertido em uma sequência que usa o caractere decimal padrão do sistema e o Microsoft Access SQL aceita somente os caracteres decimais do padrão dos EUA.

