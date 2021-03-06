---
title: Função Coalesce (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 92a7cc0a-1f9f-4969-8439-56a8d18e1347
description: Retorna a primeira expressão que não é NULL de uma lista de argumentos.
ms.openlocfilehash: af309d2330f5c3b3999a4d99d8f2ab2d6d7d61db
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411390"
---
# <a name="coalesce-function-access-custom-web-app"></a>Função Coalesce (aplicativo Web personalizado do Access)

Retorna a primeira expressão que não é NULL de uma lista de argumentos.
  
> [!NOTE]
> O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.* > Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

**Coalesce** (*Valor*, [*Valor*], ...,[*Valor*]) 
  
A **função Coalesce** contém os seguintes argumentos 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Valor*  <br/> |Uma expressão.  <br/> |
   
## <a name="remarks"></a>Comentários

Se todos os argumentos são NULL, **Coalesce retorna** NULL. 
  
## <a name="example"></a>Exemplo

A expressão a seguir é usada como regra de validação para uma tabela. A expressão garante que as entradas sejam feitas nos campos Nome, Sobrenome, Email, Telefone Celular, Telefone De Trabalho, Telefone Residência e Empresa antes da confirmação de um registro. Se qualquer um dos campos listados for deixado em branco, a função **Coalesce** retornará Null, o que viola a regra de validação. 
  
```vb
Coalesce([First Name],[Last Name],[Email],[Mobile Phone],[Work Phone],[Home Phone],[Company]) Is Not Null
```


