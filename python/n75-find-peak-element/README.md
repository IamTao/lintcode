由时间复杂度的暗示可知应使用二分搜索。首先分析若使用传统的二分搜索，若`A[mid] > A[mid - 1] && A[mid] < A[mid + 1]`，则找到一个peak为`A[mid]`;若`A[mid - 1] > A[mid]`,则A[mid]左侧必定存在一个peak，可用反证法证明：若左侧不存在peak，则`A[mid]`左侧元素必满足`A[0] > A[1] > ... > A[mid -1] > A[mid]`，与已知`A[0] < A[1]`矛盾，证毕。同理可得若`A[mid + 1] > A[mid]`，则A[mid]右侧必定存在一个peak。如此迭代即可得解。