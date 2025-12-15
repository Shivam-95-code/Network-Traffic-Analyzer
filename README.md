# Network-Traffic-Analyzer
Network Project
class Packet {
    String sourceIP;
    String destinationIP;
    String protocol;
    int size;

    Packet(String src, String dst, String proto, int size) {
        this.sourceIP = src;
        this.destinationIP = dst;
        this.protocol = proto;
        this.size = size;
    }
}

class NetworkTrafficAnalyzer {

    void analyze(Packet packet) {
        System.out.println("Source IP      : " + packet.sourceIP);
        System.out.println("Destination IP : " + packet.destinationIP);
        System.out.println("Protocol       : " + packet.protocol);
        System.out.println("Packet Size    : " + packet.size + " bytes");
        System.out.println("--------------------------------");
    }

    public static void main(String[] args) {

        NetworkTrafficAnalyzer analyzer = new NetworkTrafficAnalyzer();

        Packet p1 = new Packet("192.168.1.2", "192.168.1.10", "TCP", 1200);
        Packet p2 = new Packet("10.0.0.5", "10.0.0.8", "UDP", 800);
        Packet p3 = new Packet("172.16.0.3", "172.16.0.1", "ICMP", 300);

        analyzer.analyze(p1);
        analyzer.analyze(p2);
        analyzer.analyze(p3);
    }
}
