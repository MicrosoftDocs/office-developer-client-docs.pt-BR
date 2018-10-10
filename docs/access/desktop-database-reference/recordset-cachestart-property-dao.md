---
title: Propriedade Recordset.CacheStart (DAO)
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
ms.openlocfilehash: 7ded35253f0cea2243076db6a12caeeee22ecd09
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462541"
---
# <a name="recordsetcachestart-property-dao"></a>Propriedade Recordset.CacheStart (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Define ou retorna um valor que especifica o indicador do primeiro registro em um objeto Recordset tipo dynaset contendo dados para serem armazenados em cache localmente a partir da fonte de dados ODBC (apenas espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . CacheStart

*expressão* Uma variável que representa um objeto **Recordset** .

## <a name="remarks"></a>Comentários

Dados armazenados em cache melhoram o desempenho se você usa objetos **Recordset** para recuperar dados de um servidor remoto. Um cache é um espaço na memória local que mantém os dados mais recentemente recuperados do servidor; isso é útil quando os usuários solicitam esses dados novamente durante a execução de um aplicativo. Quando os usuários solicitam dados, o mecanismo de banco de dados do Microsoft Access verifica esses dados no cache primeiro em vez de recuperá-los do servidor, o que leva mais tempo. O cache salva apenas dados provenientes de uma fonte de dados ODBC.

Qualquer fonte de dados ODBC conectada ao mecanismo de banco de dados do Microsoft Access, como uma tabela vinculada, pode ter um cache local. Para criar o cache, abra um objeto **Recordset** a partir da fonte de dados remota, defina as propriedades **CacheSize** e **[CacheStart](recordset-cachestart-property-dao.md)** e utilize o método **[FillCache](recordset-fillcache-method-dao.md)** ou navegue pelos registros utilizando os métodos **Move**.

A configuração da propriedade **CacheStart** é o indicador do primeiro registro no objeto **Recordset** a ser armazenado em cache. Você pode usar o indicador de qualquer registro para definir a propriedade **CacheStart**. Torne o registro que deve iniciar o cache o registro atual e defina a propriedade **CacheStart** igual à propriedade **[Bookmark](recordset-bookmark-property-dao.md)**.

O mecanismo de banco de dados do Microsoft Access solicita os registros dentro do intervalo de cache, a partir do cache, e solicita os registros fora do intervalo de cache a partir do servidor.

Os registros recuperados do cache não refletem as alterações feitas simultaneamente por outros usuários na fonte de dados.

Para forçar uma atualização de todos os dados em cache, defina a propriedade **CacheSize** do objeto **Recordset** como 0, redefina-a para o tamanho do cache solicitado originalmente e use o método **FillCache**.

