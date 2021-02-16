---
title: Documentação do valor de retorno de MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c32ee53c-b063-4a00-a6bf-75ce5e07f56a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5bbafe9fda479d951bb20175ab904dc6e241226a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429688"
---
# <a name="mapi-return-value-documentation"></a>Documentação do valor de retorno de MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
As entradas de referência neste documento de referência retornam apenas os valores que exigem alguma manipulação por aplicativos cliente. Os valores de retorno que indicam condições comuns de erro e podem ser deduzidos pela verificação da falha não estão incluídos na documentação. Por exemplo, muitos métodos de interface podem retornar MAPI_E_INVALID_PARAMETER se um chamador especificar o valor errado para um parâmetro de entrada. Esse valor normalmente não está listado no conjunto de valores de retorno esperados porque não há necessidade de procurar especificamente por MAPI_E_INVALID_PARAMETER e não é necessário processá-lo de forma diferente de qualquer outro erro. Por outro lado, alguns provedores de serviços não suportam a notificação de evento e retornarão MAPI_E_NO_SUPPORT para o método **Advise** feito por clientes por meio de **IMAPISession**. Como os clientes precisam verificar explicitamente esse valor e fornecer código para lidar com a condição que ele representa caso ocorra, MAPI_E_NO_SUPPORT é incluído na lista de valores de retorno [para IMAPISession::Advise](imapisession-advise.md).
  
A tabela a seguir descreve os valores de erro que normalmente são retornados de métodos e funções e exigem tratamento explícito por parte de um cliente ou provedor de serviços. Esses valores se enquadram em quatro categorias: valores que indicam dados de entrada inválidos, valores que indicam problemas de recurso, valores que indicam incompatibilidade do conjunto de caracteres e valores que indicam falha de uma origem desconhecida.
  
|**Valor retornado**|**Descrição**|
|:-----|:-----|
|MAPI_E_INVALID_PARAMETER  <br/> |Um ou mais dos parâmetros passados para o método ou funções não eram válidos.  <br/> |
|MAPI_E_UNKNOWN_FLAGS  <br/> |Um ou mais valores para um parâmetro flags não eram válidos.  <br/> |
|MAPI_E_DISK_ERROR  <br/> |Houve um problema ao escrever no disco ou na leitura.  <br/> |
|MAPI_E_NOT_ENOUGH_DISK  <br/> |Não havia espaço em disco suficiente disponível para concluir a operação.  <br/> |
|MAPI_E_NOT_ENOUGH_MEMORY  <br/> |Não havia memória suficiente disponível para concluir a operação.  <br/> |
|MAPI_E_NOT_ENOUGH_RESOURCES  <br/> |Não havia recursos suficientes do sistema disponíveis para concluir a operação.  <br/> |
|MAPI_E_BAD_CHARWIDTH  <br/> |Existe uma incompatibilidade nos conjuntos de caracteres suportados pelo chamador e pela implementação.  <br/> |
|MAPI_E_CALL_FAILED  <br/> |Ocorreu um erro de origem inesperada ou desconhecida.  <br/> |
   
As constantes que representam valores de retorno MAPI estão listadas no MAPICODE. Arquivo de header H. Algumas das constantes mapeiam para erros win32; o mapeamento dessas constantes para valores numéricos pode ser encontrado no arquivo de título Win32, WINERROR.H.
  
Os erros relacionados a dados inválidos passados por um chamador podem ser determinados por meio das funções de API de validação de parâmetro fornecidas por MAPI ou um conjunto de macros. 
  
A incompatibilidade do conjunto de caracteres surge quando ocorre uma das seguintes situações:
  
- Um cliente ou provedor de serviços define o sinalizador MAPI_UNICODE em um método ou chamada de função e a implementação não dá suporte a Unicode. A MAPI_UNICODE indica que as cadeias de caracteres passadas como entrada são cadeias de caracteres Unicode e que as cadeias de caracteres passadas como saída devem ser cadeias de caracteres Unicode.
    
- Um cliente ou provedor de serviços não configura o sinalizador MAPI_UNICODE em um método ou chamada de função e a implementação só dá suporte a Unicode.
    

