---
title: Propriedade Relation.PartialReplica (DAO)
TOCTitle: PartialReplica Property
ms:assetid: 3cb15639-371e-06e3-e2ba-30466ce09a72
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192692(v=office.15)
ms:contentKeyID: 48544324
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053557
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 52ad71b0b9410a20fe848fb1428f3cdc83a966a8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870818"
---
# <a name="relationpartialreplica-property-dao"></a>Propriedade Relation.PartialReplica (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Define ou retorna um valor em um objeto **Relation**, indicando se essa relação deverá ser considerada durante o preenchimento de uma réplica parcial a partir de uma réplica completa. (somente em banco de dados do mecanismo de banco de dados do Microsoft Access). **Boolean** de leitura/gravação.

## <a name="syntax"></a>Sintaxe

*expressão* . PartialReplica

*expressão* Uma expressão que retorna um objeto **Relation** .

## <a name="remarks"></a>Comentários

A configuração ou o valor de retorno é um tipo de dados Boolean que será **True** quando a relação for imposta durante a sincronização.

Essa propriedade permite replicar os dados da réplica completa para a réplica parcial com base nas relações entre as tabelas. Use a propriedade **PartialReplica** quando apenas a definição da propriedade **ReplicaFilter** não especificar de forma adequada quais dados deverão ser replicados para a réplica parcial. Por exemplo, suponha que você tenha um banco de dados no qual a tabela Clientes possui uma relação um-para-muitos com a tabela Pedidos e que você queira configurar uma réplica parcial que replique apenas os pedidos dos clientes da região da Califórnia (em vez de todos os pedidos). Não é possível definir a propriedade **ReplicaFilter** na tabela Pedidos como Region = 'CA', porque o campo Região está na tabela Clientes e não na tabela Pedidos.

Para replicar todos os pedidos da região da Califórnia, indique se a relação entre as tabelas Pedidos e Clientes estará ativa durante a replicação. Assim que você tiver criado uma réplica parcial, as próximas etapas serão preenchidas com todos os pedidos da região da Califórnia:

1.  Defina a propriedade **ReplicaFilter** no objeto de clientes **TableDef** para "região = 'CA'".

2.  Defina o valor da propriedade **PartialReplica** como **True** no objeto **Relation**, que corresponde à relação entre Pedidos e Clientes.

3.  Chame o método **PopulatePartial**.
    

> [!NOTE]
> <P>Quando você definir um filtro para réplica ou uma relação de réplicas, esteja ciente de que os registros da réplica parcial que não satisfizerem os critérios de restrição serão removidos da réplica parcial, mas não da réplica completa. Por exemplo, suponha que você tenha definido a propriedade <STRONG>ReplicaFilter</STRONG> em <STRONG>TableDef</STRONG> de Clientes na réplica parcial como "Region = 'CA'" e depois tenha preenchido novamente o banco de dados. Isso inserirá ou atualizará todos os registros dos clientes da Califórnia. Se você redefinir depois a propriedade <STRONG>ReplicaFilter</STRONG> como "Region = 'FL'" e preencher novamente o banco de dados, todos os registros da região da Califórnia na réplica parcial serão removidos e todos os registros dos clientes da Flórida serão inseridos na réplica completa. Nenhum registro será excluído da réplica completa. Antes de definir a propriedade <STRONG>ReplicaFilter</STRONG> ou a propriedade <STRONG>PartialReplica</STRONG>, é uma boa ideia sincronizar a réplica parcial na qual você está definindo essas propriedades na réplica completa. Isso garantirá que as alterações pendentes na réplica parcial serão mescladas na réplica completa antes de quaisquer registros serem removidos da réplica parcial.</P>


