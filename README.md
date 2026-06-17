flowchart TD
    classDef china fill:#e3f2fd,stroke:#1565c0,stroke-width:2px;
    classDef abroad fill:#fff3e0,stroke:#e65100,stroke-width:2px;
    classDef end fill:#e8f5e9,stroke:#2e7d32,stroke-width:2px;
    classDef note fill:#f3e5f5,stroke:#6a1b9a,stroke-width:1px,dashed;

    A[<b>阶段一：生产 / 采购</b><br>⏱ 自产常规：45-60天<br>⏱ 自产快反：20-30天<br>⏱ 1688现货：3-7天<br>📄 <b>产出：生产单</b><br>（发给本地仓作收货依据）]:::china

    B[<b>阶段二：国内运输</b><br>⏱ 耗时：约7天<br>（工厂/1688 → 本地仓）<br>📄 <b>产出：供应商送货单</b>]:::china

    C[<b>阶段三：本地仓操作</b><br>⏱ 耗时：2-5天<br>📥 依据生产单核对来货<br>📄 <b>产出：收货单</b><br>📄 <b>产出：质检单（国内）</b><br>（贴标/打托/制作出口文件）]:::china

    D[<b>阶段四：头程运输 + 清关</b><br>⏱ 耗时：15-35天（海运）<br>（此段与阶段三合计20-40天）<br>📄 <b>产出：报关单</b><br>📄 <b>产出：提单（B/L）/空运单</b><br>📄 <b>产出：头程物流单</b>]:::china

    E[<b>阶段五：海外仓签收入库</b><br>⏱ 耗时：1-2天<br>📥 依据物流单 + 实物核对<br>🏢 平台：FBA / WFS / 4PX等<br>📄 <b>产出：入库单（海外）</b><br>📄 <b>产出：质检单（海外）</b><br>（区分国内质检单）]:::abroad

    F[<b>阶段六：上架与尾程派送</b><br>⏱ 耗时：2-5天<br>（买家下单→拣货打包→派送）<br>📄 <b>产出：拣货单</b><br>📄 <b>产出：发货单（海外）</b><br>📄 <b>产出：尾程物流单</b>]:::abroad

    G[<b>🏁 终点：买家签收</b><br>📄 <b>产出：签收凭证</b>]:::end

    A --> B --> C --> D --> E --> F --> G

    %% 总时长汇总
    H[<b>📅 全链路总耗时（含尾程）</b><br>常规自产：45~60 + 7 + 20~40 + 3~7<br>= <b>75~114天</b><br>快反自产：20~30 + 7 + 20~40 + 3~7<br>= <b>50~84天</b><br>1688现货采购：3~7 + 7 + 20~40 + 3~7<br>= <b>33~61天</b>]:::note

    D -.->|阶段三+四合计| H
    F -.->|尾程计入| H
    
