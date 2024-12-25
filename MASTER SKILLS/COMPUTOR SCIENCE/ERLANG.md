2024年9月4日10:46:20

[[LANGUAGE]]

行为模式
[[分布式应用]]
[[并发架构]]

[[项目学习]]
[[分布式系统学校资料]]

当前阶段目标：
实现一个分布式应用部署，
完成多个服务器的CPU利用率5分钟采集一次并且入库



---
```
prepare_target_last(Line,Posi,Regx) ->
    Map = [null,"null",<<"null">>],
    G1 = not lists:member(Line,Map),
    Blocks = binary:split(Line,Regx,[global]),
    G2 = (Posi < length(Blocks)),
    Flag = G1 and G2,
    case Flag of
        false -> Res = null;
        true ->
            ListSource = binary:split(Line,Regx,[global]),
            ListTar = [X || X <- ListSource, length(binary_to_list(X)) > 0],
            case Posi of
                0 -> Res = lists:last(ListTar);
                _ -> Res = lists:nth(Posi,ListTar)
            end
    end,
    Res.
```

