---
title: Propriedade Recordset. CacheStart (DAO)
TOCTitle: CacheStart Property
ms:assetid: 03814312-660a-d8e9-8a7b-bc14d66e05ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844802(v=office.15)
ms:contentKeyID: 48542986
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053171
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 514f109f0eed902287e519bcd7a729397e70eaa5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300613"
---
# <a name="recordsetcachestart-property-dao"></a>Propriedade Recordset. CacheStart (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Define ou retorna um valor que especifica o marcador do primeiro registro em um objeto Recordset do tipo dynaset, que contém os dados a serem armazenados localmente a partir de uma fonte de dados ODBC (somente em espaços de trabalho do Microsoft Access ).

## <a name="syntax"></a>Sintaxe

*expressão* . CacheStart

*expressão* Uma variável que representa um objeto **Recordset** .

## <a name="remarks"></a>Comentários

O cache de dados melhorará o desempenho, se você usar os objetos **Recordset** para recuperar dados de um servidor remoto. Um cache é um espaço na memória local que mantém os dados recuperados do servidor mais recentemente; isso será útil se os usuários solicitarem os dados novamente enquanto o aplicativo estiver em execução. Quando os usuários solicitarem os dados, o mecanismo do banco de dados do Microsoft Access verificará o cache dos dados solicitados primeiro em vez de recuperá-los do servidor, o que levará mais tempo. O cache salvará apenas os dados provenientes de uma fonte de dados ODBC.

Qualquer mecanismo de banco de dados do Microsoft Access conectado à fonte de dados ODBC, como uma tabela vinculada, pode ter um cache local. Para criar o cache, abra um objeto **Recordset** a partir da fonte de dados remota, defina as propriedades **CacheSize** e **[CacheStart](recordset-cachestart-property-dao.md)** e depois use o método **[FillCache](recordset-fillcache-method-dao.md)** ou consulte por etapas os registros usando os métodos **Move**.

A definição da propriedade **CacheStart** é o marcador do primeiro registro no objeto **Recordset** a ser armazenado. Use o marcador de um registro para definir a propriedade **CacheStart**. Faça o registro que quiser para iniciar o cache do período atual e defina a propriedade **CacheStart** como igual à propriedade **[Bookmark](recordset-bookmark-property-dao.md)**.

O mecanismo do banco de dados do Microsoft Access solicita registros em um intervalo de cache a partir do cache e requisita registros de fora do intervalo de cache a partir do servidor.

Os registros recuperados do cache não refletem as alterações feitas de forma simultânea com os dados da fonte de outros usuários.

Para forçar uma atualização em todos os dados armazenados, defina a propriedade **CacheSize** do objeto **Recordset** como 0, redefina-o para o tamanho de cache solicitado originalmente e depois use o método **FillCache**.

