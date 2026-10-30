# Ultima Rota - Inimigos

Repositório contendo os inimigos desenvolvidos para o projeto **Ultima Rota**, criado em Unity.

## Inimigos disponíveis

Atualmente o projeto possui três inimigos:

- Zombie Small
- Zombie Big
- Zombie Axe

Cada inimigo possui seu próprio pacote `.unitypackage`, permitindo a importação direta para outro projeto Unity.

## Funcionalidades

Os inimigos possuem:

- Perseguição automática do Player
- Animações direcionais
- Idle e movimentação
- Múltiplos ataques
- Sistema de dano
- Dano sincronizado com Animation Events
- Sistema de vida
- Animação de morte
- Sistema de drop de itens
- Suporte a diferentes valores de vida, velocidade e dano

## Arquivos

```text
Zumbi_Small.unitypackage
Zombie_Big.unitypackage
Zombie_Axe.unitypackage
```

Os pacotes incluem os scripts e assets necessários para o funcionamento dos inimigos.

## Scripts principais

```text
EnemyFollow.cs
EnemyHealth.cs
EnemyDamage.cs
EnemyDrop.cs
IDamageable.cs
```

## Importação

Para importar um inimigo em outro projeto Unity:

1. Abra o projeto no Unity.
2. Vá em `Assets`.
3. Selecione `Import Package`.
4. Clique em `Custom Package`.
5. Selecione o arquivo `.unitypackage` desejado.
6. Confirme a importação dos arquivos.

## Integração

Os inimigos procuram automaticamente um GameObject com a tag:

```text
Player
```

O sistema de dano utiliza a interface:

```text
IDamageable
```

Portanto, para integrar o dano ao jogador definitivo, o sistema de vida do Player deve implementar essa interface.

O sistema de drop atualmente também pode utilizar um objeto de teste para validar a geração de itens após a morte do inimigo.

## Observações

O Zombie Axe possui uma pequena diferença visual em alguns frames do segundo ataque lateral, mas o comportamento, dano e animações estão funcionais.

Alguns parâmetros, como vida, velocidade, intervalo entre ataques, dano e alcance, podem ser ajustados diretamente pelo Inspector do Unity.

## Projeto

**Ultima Rota**

Sistema de inimigos desenvolvido em Unity para integração com o projeto principal.