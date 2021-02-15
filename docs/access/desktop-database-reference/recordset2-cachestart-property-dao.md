---
title: Propriedade Recordset2.CacheStart (DAO)
TOCTitle: CacheStart Property
ms:assetid: 2e9c2b0d-b382-e4d6-9406-ace0e538a7b7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192239(v=office.15)
ms:contentKeyID: 48543989
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e6f68cc9704d7dafe7a1d779b338294c9d5fc1c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307417"
---
# <a name="recordset2cachestart-property-dao"></a>Propriedade Recordset2.CacheStart (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Define ou retorna um valor que especifica o marcador do primeiro registro em um objeto Recordset do tipo dynaset, que contém os dados a serem armazenados localmente a partir de uma fonte de dados ODBC (somente em espaços de trabalho do Microsoft Access ).

## <a name="syntax"></a>Sintaxe

*expressão* . CacheStart

*expressão* Uma variável que representa **um objeto Recordset2** .

## <a name="remarks"></a>Comentários

O cache de dados melhorará o desempenho, se você usar os objetos **Recordset** para recuperar dados de um servidor remoto. Um cache é um espaço na memória local que mantém os dados recuperados do servidor mais recentemente; isso será útil se os usuários solicitarem os dados novamente enquanto o aplicativo estiver em execução. Quando os usuários solicitarem os dados, o mecanismo do banco de dados do Microsoft Access verificará o cache dos dados solicitados primeiro em vez de recuperá-los do servidor, o que levará mais tempo. O cache salvará apenas os dados provenientes de uma fonte de dados ODBC.

Qualquer mecanismo de banco de dados do Microsoft Access conectado à fonte de dados ODBC, como uma tabela vinculada, pode ter um cache local. Para criar o cache, abra um objeto **Recordset** a partir da fonte de dados remota, defina as propriedades **CacheSize** e **[CacheStart](recordset2-cachestart-property-dao.md)** e depois use o método **[FillCache](recordset2-fillcache-method-dao.md)** ou consulte por etapas os registros usando os métodos **Move**.

A definição da propriedade **CacheStart** é o marcador do primeiro registro no objeto **Recordset** a ser armazenado. Use o marcador de um registro para definir a propriedade **CacheStart**. Faça o registro que quiser para iniciar o cache do período atual e defina a propriedade **CacheStart** como igual à propriedade **[Bookmark](recordset2-bookmark-property-dao.md)**.

O mecanismo do banco de dados do Microsoft Access solicita registros em um intervalo de cache a partir do cache e requisita registros de fora do intervalo de cache a partir do servidor.

Os registros recuperados do cache não refletem as alterações feitas de forma simultânea com os dados da fonte de outros usuários.

Para forçar uma atualização em todos os dados armazenados, defina a propriedade **CacheSize** do objeto **Recordset** como 0, redefina-o para o tamanho de cache solicitado originalmente e depois use o método **FillCache**.

